# Home Assistant Groups
> Groups integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Groups section include groups from different entities

### Groups
* Woonkamer
* Badkamer
* Slaapkamer
* Keuken
* Gang

**group.yaml**
```yaml
livingroom:
  name: Woonkamer
  entities:
    - light.lighten_woonkamer

```