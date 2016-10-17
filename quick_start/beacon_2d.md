<!--
The MIT License (MIT)

Copyright (c) 2014, 2015 IBM Corporation
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
-->

# BLE Beacon Placement & Fingerprinting (for 2D)

This section describes how to set up beacons on your site and collect data for localization for 2D.

## Overview

* Prepare [LocationService server](https://github.com/hulop/BLELocalization)
* Prepare 2D sampling tool (to be opensourced)
* Edit floorplans
* Do sampling
* Compose data for localization

### Edit floorplans

* open LocationService/floorplans.html
* click "add a floorplan" to add a floorplan image with some parameters
 * Image file: floorplan image to be rendered at an anchor
 * Group: specify same string for same building floorplans
 * Floor: 0=1st floor, 1=2nd floor, ..., -1=1st basement
 * Origin: origin of the floorplan where rendered on the anchor  
   (You can input the value by clicking on map when the form is selected)
 * PPM: scale factor for the image (pixel per meter)  
   (You can input the value by clicking two points on the map and specifying value in meter, when the form is selected)
* submit it
* click "map" button of your floorplan
 * you can see the local coordinate map in Floorplan section and the global coordinate map in Anchor section
* edit anchor
 * latitude/longitude: where floorplan origin is located
 * rotate: -180~180 degree value of rotation (0 = up, 90 = right, -90 = left)
 * opacity: image opacity value
* save anchor

**Floorplan** is an image of indoor place. 

### Do sampling

#### Preparation
* open LocationService/sampling.html
* click "add a reference point"
 * Name/Comment: for your convenience
 * Floor: select floor plan 
 * X / Y: local origin for sampling (you can input by clicking on the map)  
 * Rotate: -180 ~ 180 degree  
   **hint**: corner of a room / corridor is easy to match the position of the map and the position in the real environment. 

**Reference Point** is an local origin for sampling. You might want to devide areas, if you have large indoor space for sampling. At least one reference point is needed for the sampling tool.  

#### Sampling
* open 2D sampling tool
* select "Settings" tab
 * Server host: specify server host (with a port) of LocationService
 * Beacon UUID: specify beacon UUID to be sampled
 * Site ID: for your convenience
* back to "Beacons" tab
 * Select reference point
 * Specify x, y and z, (z is for height of the standing position from the floor, it is usually 0)  
   x=right, y=up coordinat from the reference origin
 * +/- button to adjust number of sampling
 * **10 or more is recommended (1 sampling per second)**
* click "start" to start sampling
 * **turning 360 degree at the position while sampling might improve robustness**	
 * number of beacons beeing sampled is shown
 * the sampling data will be sent to the server automatically
 * "Retry" button will be shown if there is networking error

### Compose data for localization
* open LocationService/2dMapData/ and compose data into one single json
 * Anchor: origin of the sampling data xy-coordinate
 * Samples: csv files of sampling data  
   you can download csv file at LocationService/sampling.html
 * Beacons: csv files of beacon data  
   you can edit / export beacon data at LocationService/floorplans.html
 * Layers: images of wall model for localization. You should specify every floors on which sampling data are collected.
 * ObservationModelParameters: This will be caluculated automatically but it may take time. You can specify trained model here as cache.   
 (see [BasicLocalizer tool in HULOP/blelocpp](https://github.com/hulop/blelocpp))