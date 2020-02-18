# Home Assistant Notifiers
> Notifiers integration

[![Build Status](https://travis-ci.org/pascalwilbrink/ha-config.svg?branch=master)](https://travis-ci.org/pascalwilbrink/ha-config)

Home Assistant Notifiers section include different notifiers from different sources

### Sources
* [Telegram](#telegram)

## Telegram
[Telegram](https://telegram.org) is a chat messaging app for Windows/Linux/OSX and Android/IOS.

### Setup

**notify.yaml**
```yaml
- name: Telegram
  platform: telegram
  chat_id: !secret telegram_chat_id
```

**secrets.yaml**
```yaml
telegram_chat_id: [CHAT_ID_FROM_TELEGRAM]
```