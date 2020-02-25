# Home Assistant Zones
> Zones integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Zones section include zones. 
Each yaml file is included by configuration.yaml with ``` !include_dir_list zones/```

## Zones
* [Home](#home)
* [Parents](#parents)
* [Work](#work)

### Home
| Name      | Value    | 
|-----------|----------|
| Name      | Home     |
| Latitude  | [secret] | 
| Longitude | [secret] |
| radius    | 50       |
| icon      | mdi:home |


### Parents
| Name      | Value             | 
|-----------|-------------------|
| Name      | Parents           |
| Latitude  | [secret]          | 
| Longitude | [secret]          |
| radius    | 50                |
| icon      | mdi:account-group |


### Work
| Name      | Value         | 
|-----------|---------------|
| Name      | Work          |
| Latitude  | [secret]      | 
| Longitude | [secret]      |
| radius    | 50            |
| icon      | mdi:briefcase |


## Example
```yaml
name: Home
latitude: !secret zone_home_lat
longitude: !secret zone_home_lng
radius: 50
icon: mdi:home
```