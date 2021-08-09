## Profile Interpolation Custom Device ##

**Profile Interpolation Custom Device** allows the user to implement a profile interpolation lookup based on a CSV file. The typical use case for this add-on allows for interpolation of a defined set of position vs. load profiles that will ultimatley be used as the load setpoint in a PID controller. 

## Basic Mode ##

Limit Checking Disabled

**Functional Diagram**
![Functional Diagram](https://github.com/NIVeriStandAdd-Ons/Profile-Interpolation-Custom-Device/blob/master/Source/System%20Explorer/Docs/Functional%20Diagram%20wo%20Limits.PNG)

**Example Table**:

| Profile Name  | Position (revs) |   Load (lbs) |
| :-----------: | :-------------: | :----------: |
|  Profile #1   |        0        |         0    |
|  Profile #1   |        5        |        50    |
|  Profile #1   |       10        |       100    |
|  Profile #1   |       20        |       200    |
|  Profile #2   |        0        |         0    |
|  Profile #2   |        5        |       500    |

## Advanced Mode ##

Limit Checking Enabled

Upper and lower limits can be defined for each point in the table to take advantage real-time limit checking of the measured load. Limit Enable and Load (Measured) channels are used to control the output of the limit check and results are indicated by the Load (Limit Violation) channel.

**Functional Diagram**
![Functional Diagram](https://github.com/NIVeriStandAdd-Ons/Profile-Interpolation-Custom-Device/blob/master/Source/System%20Explorer/Docs/Functional%20Diagram%20w%20Limits.PNG)

**Example Table**

| Profile Name  | Position (revs) |   Load (lbs) |  Lower Limit (lbs) |  Upper Limit (lbs) |
| :-----------: | :-------------: | :----------: | :----------------: | :----------------: |
|  Profile #1   |        0        |         0    |          -10       |          10        |
|  Profile #1   |        5        |        50    |           40       |          60        |
|  Profile #1   |       10        |       100    |           90       |         110        |
|  Profile #1   |       20        |       200    |          190       |         210        |
|  Profile #2   |        0        |         0    |          -10       |          10        |
|  Profile #2   |        5        |       500    |          490       |         510        |

## Misc Information ##

### LabVIEW Source Version ###

LabVIEW 2020

### Built Availability ###

Builds available for VeriStand 2019 & 2020 under releases.

### Quality, Limitations ###

This IP is new. 

### Built Dependencies ###

N/A

### Source Dependencies ###

[OpenG Array Library 4.1.1.14 or Higher] vipm://oglib_array?repo_url=http://www.jkisoft.com/packages

[NI VeriStand Addon Inline-Async-APIs 1.0.0 or Higher] https://github.com/ni/niveristand-custom-device-inline-async-api/releases/tag/v1.0.0

### License ###

This source code and all releases are provided under the Apache 2.0 open-source software license.

 Copyright 2021 National Instruments
 

  Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.
  You may obtain a copy of the License at 
  http://www.apache.org/licenses/LICENSE-2.0
  Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and limitations under the License.
