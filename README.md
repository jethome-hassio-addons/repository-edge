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

<https://github.com/jethome-hassio-addons/repository>

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
![Supports aarch64 Architecture][jethub-mqtt-io-aarch64-shield]
![Supports amd64 Architecture][jethub-mqtt-io-amd64-shield]

Expose JetHome JetHub peripheral (relays, inputs, etc..) via mqtt-io

[:books: JetHome JetHub mqtt-io peripheral exposer add-on documentation][addon-doc-jethub-mqtt-io]

### &#10003; [JetHome peripheral exposer][addon-jethub-gpio2mqtt]

![Latest Version][jethub-gpio2mqtt-version-shield]
![Supports aarch64 Architecture][jethub-gpio2mqtt-aarch64-shield]
![Supports amd64 Architecture][jethub-gpio2mqtt-amd64-shield]

Expose JetHome JetHub (D1/D2/D3/H1) peripheral (relays, inputs, UXM control) via gpio2mqtt

[:books: JetHome peripheral exposer add-on documentation][addon-doc-jethub-gpio2mqtt]

## Releases

Add-on releases are **NOT** based on [Semantic Versioning][semver], unlike
all our other repositories. The latest build commit SHA hash of each
add-on, represents the version number.

## Support

- [Open an issue for the add-on: JetHome JetHub mqtt-io peripheral exposer][jethub-mqtt-io-issue]
- [Open an issue for the add-on: JetHome peripheral exposer][jethub-gpio2mqtt-issue]

[addon-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/tree/8d42fa9
[addon-doc-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/blob/8d42fa9/README.md
[jethub-mqtt-io-issue]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/issues
[jethub-mqtt-io-version-shield]: https://img.shields.io/badge/version-8d42fa9-blue.svg
[jethub-mqtt-io-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[jethub-mqtt-io-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[addon-jethub-gpio2mqtt]: https://github.com/jethome-hassio-addons/addon-jethub-gpio2mqtt/tree/485315a
[addon-doc-jethub-gpio2mqtt]: https://github.com/jethome-hassio-addons/addon-jethub-gpio2mqtt/blob/485315a/README.md
[jethub-gpio2mqtt-issue]: https://github.com/jethome-hassio-addons/addon-jethub-gpio2mqtt/issues
[jethub-gpio2mqtt-version-shield]: https://img.shields.io/badge/version-485315a-blue.svg
[jethub-gpio2mqtt-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[jethub-gpio2mqtt-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg

[issue]: https://github.com/jethome-hassio-addons/repository-edge/issues
[license-shield]: https://img.shields.io/github/license/jethome-hassio-addons/repository-edge.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2026.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[semver]: http://semver.org/spec/v2.0.0.html