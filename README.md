# Seeed ArduPy MMA7660 [![Build Status](https://api.travis-ci.com/Seeed-Studio/seeed-ardupy-mma7660.svg?branch=master)](https://travis-ci.com/github/Seeed-Studio/seeed-ardupy-mma7660)

## Introduction

3-Axis Digital Accelerometer is the key part in projects like orientation detection, gesture detection and Motion detection. This 3-Axis Digital Accelerometer(±1.5g) is based on Freescale's low power consumption module, MMA7660FC. It features up to 10,000g high shock survivability and configurable Samples per Second rate. For generous applications that don't require too large measurement range, this is a great choice because it's durable, energy saving and cost-efficient.

You can get more information in here [Accelerometer_MMA7660](https://github.com/Seeed-Studio/Accelerometer_MMA7660).

![Accelerometer_MMA7660](https://camo.githubusercontent.com/7bf276cb24f335bd7082dadd8d521cecaaef43af/68747470733a2f2f73746174696373332e736565656473747564696f2e636f6d2f696d616765732f313031303230303339253230312e6a7067)

## How to binding with ArduPy
- Install [AIP](https://github.com/Seeed-Studio/ardupy-aip)
- Build firmware with Seeed ArduPy MMA7660
```shell
aip install Seeed-Studio/seeed-ardupy-mma7660
aip build
```
- Flash new firmware to you ArduPy board
```shell
aip flash 
```
For more examples of using AIP, please refer to [AIP](https://github.com/Seeed-Studio/ardupy-aip).

## Usage

```python
from arduino import grove_3ada
import time

ada = grove_3ada() # SCL & SDA as the default

while True:
    print (
        "x =", ada.x, ",",
        "y =", ada.y, ",", 
        "z =", ada.z
    )
    print (
        "x-a =", ada.x_acceleration, "g,", 
        "y-a =", ada.y_acceleration, "g,", 
        "z-a =", ada.z_acceleration)
    time.sleep(1)
```

## API Reference

- **x** : Get X-axis value
```python
print(ada.x)
```

- **y** : Get Y-axis value
```python
print(ada.y)
```

- **z** : Get Z-axis value
```python
print(ada.z)
```
- **x_acceleration** : Get X-axis acceleration
 ```python
print(ada.x_acceleration)
```
- **y_acceleration*** : Get Y-axis acceleration
```python
print(ada.y_acceleration)
```
- **z_acceleration*** : Get Z-axis acceleration
```python
print(ada.z_acceleration)
```


----

This software is written by seeed studio<br>
and is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt for more information.<br>

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>


