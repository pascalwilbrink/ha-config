# Home Assistant Calendars
> Calendars integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Calendars section include calendars from different sources


### Sources
* [Todoist](#todoist)


## Todoist
[Todoist](https://todoist.com/) is a free TO-DO app for IOS and Android.

### Setup

**calendar.yaml**
```yaml
- platform: todoist
  token: !secret todoist_api_token
```

**secrets.yaml**
```yaml
todoist_api_token: [TOKEN_FROM_TODOIST]
```