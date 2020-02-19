# Home Assistant Binary Sensors
> Binary Sensors integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Binary Sensors section include binary_sensors

### Sensors
* Presence sensor (sensor by device tracker. can be overridden by input_boolean)

**binary_sensor.yaml**
```yaml
- platform: template
  sensors:
    presence:
      device_class: presence
      friendly_name: "Presence"
      entity_id:
       - input_boolean.automatic_presence
       - input_boolean.presence
       - device_tracker.pascal_htcu12
      value_template: >-
        {{    
             (is_state('input_boolean.automatic_presence', 'on') and is_state('device_tracker.pascal_htcu12', 'home'))
          or (is_state('input_boolean.automatic_presence', 'off') and is_state('input_boolean.presence', 'on'))
        }}

```