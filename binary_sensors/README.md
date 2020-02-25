# Home Assistant Binary Sensors
> Binary Sensors integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Binary Sensors section include binary_sensors

### Sensors
* Home Occupancy sensor (sensor by device tracker. can be overridden by input_boolean)

**binary_sensor.yaml**
```yaml
- platform: template
  sensors:
    home_occupancy:
      device_class: occupancy
      friendly_name: 'Occupancy'
      entity_id:
       - input_boolean.automatic_home_occupancy
       - input_boolean.home_occupancy
       - device_tracker.pascal_htcu12
      value_template: >-
        {{    
             (is_state('input_boolean.automatic_home_occupancy', 'on') and is_state('device_tracker.pascal_htcu12', 'home'))
          or (is_state('input_boolean.automatic_home_occupancy', 'off') and is_state('input_boolean.home_occupancy', 'on'))
        }}

```