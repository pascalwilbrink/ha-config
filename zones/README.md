# Home Assistant Zones
> Zones integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Zones section include zones

### Setup

**zone.yaml**
```yaml
- name: Home
  latitude: !secret zone_home_lat
  longitude: !secret zone_home_lng
  radius: 50
  icon: mdi:home
```

**secret.yaml**
```yaml
zone_home_lat: 0.00000
zone_home_lng: 0.00000
```