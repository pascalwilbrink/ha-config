# Home Assistant Sensors
> Sensors integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Sensors section include sensors

## Sensors
* [Travel Time](#travel-time)


### Travel Time
The travel time sensors return the travel time to a specific destination (latitude / longitude) with an origin based on a device-tracker.
#### Setup

**sensor.yaml**
```yaml
- name: Travel time to home
  platform: waze_travel_time
  origin: device_tracker.pascal_htcu12
  destination: !secret waze_home_destination
  region: 'EU'
```

**secret.yaml**
```yaml
waze_home_destination: 0.00000, 0.00000
```
