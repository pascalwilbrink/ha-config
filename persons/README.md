# Home Assistant Persons
> Persons integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

#### Setup

**person.yaml**
```yaml
- name: Pascal
  id: unique_id
  user_id: [USER_OF_ACCOUNT]
  device_trackers:
    - 
    - 
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