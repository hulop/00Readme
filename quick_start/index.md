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

# Quick Start Guide  
This document is for people who want to provide blind navigation support.
This document describes how to build **map** for indoor navigation-able field with iPhone and iBeacon.

## Navigation methods
NavCog Version 2 supports the following two navigation methods. When you select a map, navigation method will be automatically selected based on map data.
- 1D
   - NavCog handles edge as one-dimensional line. only beacon data is used for localization.
   - NavCog Version 1 only supports 1D method.
- 1D PDR (Pedestrian Dead Reckoning)
   - On 1D PDR method, NavCog also handles edge as one-dimensional line as same as 1D method. Acceleration sensor data will be used for localization in addition to beacon data.
   
[NavCog Version 3](https://github.com/hulop/NavCogIOSv3) supports the 2D mode. 
See [wiki](https://github.com/hulop/NavCogIOSv3/wiki) for setting up NavCog Version 3.
- 2D
   - On 2D method, NavCog handles edge as two-dimensional line. Acceleration sensor data will be used for localization in addition to beacon data.

## Prerequisites
Please prepare the following items to create and test your navigation map.

0. Mac
0. iPhone 6 or later
0. NavCov app downloaded from App Store (Please download from [App Store](https://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=1042163426&mt=8))
0. Bluetooth LE Beacon ([see Appendix](appendix.md#beacon))
0. Floor plan images (optional)
0. Long measure tape & sticky tape


## Overview of Building Map
NavCog App is utilizing Bluetooth radio wave signals to estimate user's location.
You can easily create navigation map with the following steps.


## Steps
1.	Choose target area and navigation routes in your site ([Sec. 2](map.md#add_area))
2.	Distribute beacons around the routes ([Sec. 3](beacon.md#beacon_placement))
3.	Prepare **fingerprinting** ([*1](#footnote1)) data for localization ([Sec. 3](beacon.md#fingerprinting))
4.	Build map data for the app ([Sec. 2](map.md#export_map))
5.	Test the app with your map ([Sec. 4](test.md))
6.	Submit the map data for public use ([Sec. 4](test.md#submit_map))
7.	Let your blind users try blind navigation in your site ([Sec. 5](navcog.md))

# Index

1. Index (this document)
2. [Edit Map & Routes](map.md)
3. [BLE Beacon Placement & Fingerprinting](beacon.md)
4. [Test Your Map](test.md)
5. [NavCog User Guide](navcog.md)
6. [Notice for use of battery powered beacons](battery.md)
7. [Appendix](appendix.md)

<a name="footnote1">*1</a>: Observe radio signal strength in the real environment.
