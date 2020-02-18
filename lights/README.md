# Home Assistant Lights
> Lights integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Lights section include light groups

### Setup

**light.yaml**
```yaml
- platform: group
  name: Lichten woonkamer
  entities:
    - light.woonkamer
```