# Home Assistant Add-on: JetHome JetHub peripheral exposer

[![Release][release-shield]][release] ![Project Stage][project-stage-shield] ![Project Maintenance][maintenance-shield]

## About

Expose [JetHome JetHub](https://jethome.com) resources (relays,inputs,etc..) to Home Assistant via gpio2mqtt

This addon uses the new gpio2mqtt MQTT topic structure, which changes the entity IDs
in Home Assistant compared to the legacy jethub-mqtt-io addon.
Do not run both addons at the same time — they claim the same GPIO lines.

**Note**: _All used GPIOs will **disappear** from **/sys/class/gpio** during addon run_

**Warning:** The auto-detection option works only on HAOS (Home Assistant Operating System).
For Home Assistant Supervised, please select your device manually in the configuration.


## Supported devices:

### [JetHome JetHub D1/D1+](https://jethome.ru/d1p) (Basic version with 3 relays, 4 inputs and 1-wire, 1 ZigBee module).

**Exposed peripheral:**

- 3 relays
- 4 inputs
- internal stat LED (green/red)
- (optional) ZigBee module control (BOOT, RESET)

### [JetHome JetHub H1](https://jethome.ru/h1) (Basic version, ZigBee module)

**Exposed peripheral:**

- internal stat LED
- (optional) modules slot control (BOOT, RESET)

### [JetHome JetHub D3-mini](https://docs.iot.jethome.com) (modular controller, 4 UXM slots)

**Exposed peripheral:**

- UXM slots control (RESET, MODE)

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

<https://github.com/jethome-hassio-addons/repository>


## JetHome resources:

- Documentation - https://docs.jethome.com
- Official website - https://jethome.com
- Telegram news channel - https://t.me/jethome_news
- Telegram english news channel - https://t.me/jethome_iot_news
- Telegram official chat - https://t.me/jethomeru
- Telegram official english chat - https://t.me/jethome_iot
- GitHub: https://github.com/jethome-iot

[maintenance-shield]: https://img.shields.io/maintenance/yes/2026.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[release-shield]: https://img.shields.io/badge/version-8d71208-blue.svg
[release]: https://github.com/jethome-hassio-addons/addon-jethub-gpio2mqtt/tree/8d71208