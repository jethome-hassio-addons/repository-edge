# Home Assistant Add-on: JetHome JetHub peripheral exposer

[![Release][release-shield]][release] ![Project Stage][project-stage-shield] ![Project Maintenance][maintenance-shield]

## About

Expose [JetHub](http://jethome.ru) resources (relays,inputs,etc..) to Home Assistant via [mqtt-io](https://github.com/flyte/mqtt-io)

**Note**: _All used GPIOs will **disappear** from **/sys/class/gpio** during addon run_

## Supported devices:

### [JetHome JetHub D1](http://jethome.ru/jethub-d1) (Basic version with 3 relays, 4 inputs and 1-wire).

**Exposed peripheral:**

- 3 relays
- 4 inputs
- internal stat LED (green/red)

**Note**: _You still need to use native Home Assistant [1-Wire](https://www.home-assistant.io/integrations/onewire/) integration to expose 1-Wire device 
like temperature sensors `DS18B20`_

## WARNING! THIS IS AN EDGE VERSION!

This Home Assistant Add-ons repository contains edge builds of add-ons.
Edge builds add-ons are based upon the latest development version.

- They may not work at all.
- They might stop working at any time.
- They could have a negative impact on your system.

This repository was created for:

- Anybody willing to test.
- Anybody interested in trying out upcoming add-ons or add-on features.
- Developers.

If you are more interested in stable releases of our add-ons:

<https://github.com/jethome-ru/hassio-repository>


## JetHome resources:

- Documentation - https://wiki.jethome.ru 3
- Official website - http://jethome.ru 2
- Telegram news channel - https://t.me/jethome_news
- Telegram official chat - https://t.me/jethomeru
- GitHub: https://github.com/jethome-ru 1
- E-Store: http://jhome.ru 2
- Instagram - https://instagram.com/jethomeru

[maintenance-shield]: https://img.shields.io/maintenance/yes/2021.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[release-shield]: https://img.shields.io/badge/version-fe78d85-blue.svg
[release]: https://github.com/jethome-ru/hassio-addon-jethub-mqtt-io/tree/fe78d85