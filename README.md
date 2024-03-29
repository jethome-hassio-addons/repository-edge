# EDGE - JetHome Home Assistant Add-ons

![Project Stage][project-stage-shield]
![Maintenance][maintenance-shield]

## WARNING! THIS IS AN EDGE REPOSITORY

This  repository contains edge builds of add-ons. Edge
builds add-ons are based upon the latest development version.

- They may not work at all.
- They might stop working at any time.
- They could have a negative impact on your system.

This repository was created for:

- Anybody willing to test.
- Anybody interested in trying out upcoming add-ons or add-on features.
- Developers.

If you are more interested in stable releases of our add-ons:

<https://github.com/jethome-ru/hassio-repository>

## Installation

Adding this add-ons repository to your Home Assistant instance is
pretty straightforward. In the Home Assistant add-on store,
a possibility to add a repository is provided.

Use the following URL to add this repository:

```txt
https://github.com/jethome-hassio-addons/repository-edge
```

## Add-ons provided by this repository

### &#10003; [JetHome JetHub mqtt-io peripheral exposer][addon-jethub-mqtt-io]

![Latest Version][jethub-mqtt-io-version-shield]
![Supports armhf Architecture][jethub-mqtt-io-armhf-shield]
![Supports armv7 Architecture][jethub-mqtt-io-armv7-shield]
![Supports aarch64 Architecture][jethub-mqtt-io-aarch64-shield]
![Supports amd64 Architecture][jethub-mqtt-io-amd64-shield]
![Supports i386 Architecture][jethub-mqtt-io-i386-shield]

Expose JetHome JetHub peripheral (relays, inputs, etc..) via mqtt-io

[:books: JetHome JetHub mqtt-io peripheral exposer add-on documentation][addon-doc-jethub-mqtt-io]

## Releases

Add-on releases are **NOT** based on [Semantic Versioning][semver], unlike
all our other repositories. The latest build commit SHA hash of each
add-on, represents the version number.

## Support

- [Open an issue for the add-on: JetHome JetHub mqtt-io peripheral exposer][jethub-mqtt-io-issue]

[addon-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/tree/2ab1e40
[addon-doc-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/blob/2ab1e40/README.md
[jethub-mqtt-io-issue]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/issues
[jethub-mqtt-io-version-shield]: https://img.shields.io/badge/version-2ab1e40-blue.svg
[jethub-mqtt-io-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[jethub-mqtt-io-amd64-shield]: https://img.shields.io/badge/amd64-no-red.svg
[jethub-mqtt-io-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[jethub-mqtt-io-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[jethub-mqtt-io-i386-shield]: https://img.shields.io/badge/i386-no-red.svg

[issue]: https://github.com/jethome-hassio-addons/repository-edge/issues
[license-shield]: https://img.shields.io/github/license/jethome-hassio-addons/repository-edge.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2023.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[semver]: http://semver.org/spec/v2.0.0.html