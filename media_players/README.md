# Home Assistant Media Players
> Media Players integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Media Players section include media players

### Setup

**media_player.yaml**
```yaml
- platform: androidtv
  name: 'Android TV'
  host: 192.168.2.2
  adb_server_ip: 127.0.0.1
  adb_server_port: 5037
```