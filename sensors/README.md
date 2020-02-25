# Home Assistant Sensors
> Sensors integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Sensors section include sensors.
Each yaml file is included by configuration.yaml with ``` !include_dir_list sensors/```

## Sensors
* [P2000](#p2000)
* [Time Date](#time-date)
* [Trakt](#trakt)
* [Travel Time to Home](#travel-time-to-home)
* [Travel Time to Work](#travel-time-to-work)
* [Travis CI](#travis-ci)

### P2000
The p2000 sensor returns the latest

| Name     | Value |
|----------|-------|
| platform | p2000 |
| regios   | 4     |
| radius        | 20000 |
| scan_interval | 30
platform: p2000
regios: 4
radius: 20000
scan_interval: 30
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

### Travis CI
The Travis CI sensor shows the latest builds from [https://travis-ci.org](Travis CI).
### Setup

**sensor.yaml**
```yaml
- platform: travisci
  api_key: !secret github_api_key
```

**secret.yaml**
```
github_api_key: FAKE_API_KEY
```

### Season
The Season sensor shows which season it is for automations.

**sensor.yaml**
```yaml
- platform: season
```