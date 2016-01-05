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


# Notice for use of battery powered beacons 
In general, bluetooth beacons are powered by battery or USB. 
The battery powered beacon is more popular as it is flexibility to be deployed. 
However in long term (more than two month) beacon deployment, you need to keep maintaining batteries.
Please refer to the following information to minimize maintenance cost of battery.

## Battery capacities
Battery type and capacity for typical 3V beacons are as follows. Larger capacity battery has longer battery life.

| Type of battery | Capacity |
|---------------------|---------|
| 1 x CR2477 (Lithium)| 1000mAh |
| 2 x AA (Alkaline)   | 2000mAh - 2700mAh (Manufacturer dependent) |
| 2 x AA (Lithium)    | 3000mAh | 

2 x AA (Lithium) powered beacon have 3 times battery life of CR2477 powered beacon.

In cool environment, Lithium battery is better than alkaline battery.

## Beacon settings and battery life
Battery life of beacon will strongly depend on advertising interval and transmission power settings.

Power consumption rate of 100ms advertising interval is 2 times of 200ms advertising interval.
Increasing transmission power also consumes battery power.

Advertising interval value is critical for beacon performance and it also affect user experience.
Please contact beacon vendor for optimum settings.

## How to check battery level
* LED indicator
 * Some beacon has LED indicator for battery level.
   LED color changes on dead battery level.
   Please contact beacon vendor for details.
* Beacon management tools
 * Some beacon vendor support battery level checker with special application program.
   Please contact beacon vendor for details. 
* Voltage meter
 * If none of above indicator is available, you need to remove battery from beacon then use voltage meter to check battery level.
* RSSI level  
 * If it is very hard to remove battery, you can check RSSI level using general-purpose beacon check tools such as Beacon Ranging (https://itunes.apple.com/jp/app/beacon-ranging/id734155067). 
   You can find beacons which already dead (Typically less than 0.7v on AA battery). 
   Please note it is too late to replace battery at this timing. Please replace battery before it dies.  

## When should you replace battery?
Please replace battery when battery level becomes less then the following voltage even if beacon is still working. 

| Type of Battery | Dead battery voltage |
|--------|------|
| CR2477 | 2.0V |
| AA	 | 1.0V |

Alkaline battery will cause electrolyte leakage if you leave it after dead voltage.
