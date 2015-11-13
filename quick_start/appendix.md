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


# Appendix


## <a name="transition"></a>Transition Node

Transition will be used at staircases, elevators, and double doors at entrance where the blind users can easily follow the building structure without localization support.
You should describe about transition so that the user can follow some object to get the next node.

You need to set `maxDist`, `minDist` values for edge information and `target knn` dist and `pos`.


### <a name="knnDist"></a>knnDist

You need to input maximum and minimum knn distance to all of the edges.

You can get those values as minDist/maxDist in accuracy evaluation result file.
[Accuracy Evaluation](beacon.md#acc_eval)
Please input the values of the edge on map editor.


## Beacon Type

There are some types of beacons; Battery, USB powered, water proof, embedded in LED light, and so on.

Type | Pros | Cons
---|---|---
Battery|most popular type, inexpensive|need to replace battery
USB powered|maintenance free|need power tap, expensive
Water proof|can be deployed outside|usually power is battery, expensive
LED light|maintenance free|need socket, expensive

##BLE Beacon Protocol

As of October 2015, there are three BLE beacon protocol. Currently NavCog supports iBeacon.

* [iBeacon (Apple)](https://developer.apple.com/ibeacon/)
* [EddyStone (Google)](https://developers.google.com/beacons/?hl=en)
* [AltBeacon (Radius Network)](http://altbeacon.org)
