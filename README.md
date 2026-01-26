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
![Supports aarch64 Architecture][jethub-mqtt-io-aarch64-shield]
![Supports amd64 Architecture][jethub-mqtt-io-amd64-shield]

Expose JetHome JetHub peripheral (relays, inputs, etc..) via mqtt-io

[:books: JetHome JetHub mqtt-io peripheral exposer add-on documentation][addon-doc-jethub-mqtt-io]

## Releases

Add-on releases are **NOT** based on [Semantic Versioning][semver], unlike
all our other repositories. The latest build commit SHA hash of each
add-on, represents the version number.

## Support

- [Open an issue for the add-on: JetHome JetHub mqtt-io peripheral exposer][jethub-mqtt-io-issue]

[addon-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/tree/fd3152f
[addon-doc-jethub-mqtt-io]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/blob/fd3152f/README.md
[jethub-mqtt-io-issue]: https://github.com/jethome-hassio-addons/addon-jethub-mqtt-io/issues
[jethub-mqtt-io-version-shield]: https://img.shields.io/badge/version-fd3152f-blue.svg
[jethub-mqtt-io-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[jethub-mqtt-io-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg

[issue]: https://github.com/jethome-hassio-addons/repository-edge/issues
[license-shield]: https://img.shields.io/github/license/jethome-hassio-addons/repository-edge.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2026.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[semver]: http://semver.org/spec/v2.0.0.html