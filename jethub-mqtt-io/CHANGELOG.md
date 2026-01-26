# Changelog since v0.3.0
- docs: update README template

- Fix shields.io badge for versions with hyphens (escape - as --)
- Update links to HTTPS
- Add warning about auto-detection requiring HAOS
- Add English Telegram channels
- Update product page URLs 
- feat(detect-model): add /proc/cmdline detection method

Add fallback detection via board= parameter in /proc/cmdline:
- jethub-j80 -> jethub-h1
- jethub-j100 -> jethub-d1
- jethub-j200 -> jethub-d2

Also improve error reporting - each detection method now outputs
its specific error message immediately after failure. 
- fix(dockerfile): add hadolint ignore for DL4006 and SC1091 
- fix(dockerfile): restore binary rename for correct arch 
- fix(dockerfile): use multi-arch manifest and dev tag directly

- Use multi-arch OCI manifest (remove -${ARCH} suffix from tag)
- For dev channel use 'dev' tag directly instead of reading from JSON
- Simplify binary download (artifact now named 'gpio2mqtt') 
- feat: add gpio2mqtt-versions.json for dynamic binary versioning

- Create gpio2mqtt-versions.json to track binary versions per channel
- Modify gpio2mqtt-trigger.yaml to update JSON on dispatch events
- Update Dockerfile to read version from JSON based on addon version
- Remove hardcoded BINARY_VERSION from build.yaml

Channel detection:
- Version with rc/beta -> beta channel
- Pure semver (X.Y.Z) -> stable channel
- Everything else -> dev channel 
- Update description 
- Merge pull request #54 from jethome-hassio-addons/fix/gpio2mqtt-legacy-mqttio-config

fix(config): add legacy_mqttio compatibility settings 
- feat(config): add legacy_mqttio as configurable addon option

- Add legacy_mqttio option to config.yaml (default: true)
- Add schema validation (bool, always visible in UI)
- Dynamically inject legacy_mqttio in entrypoint.sh
- Remove hardcoded legacy_mqttio from static configs

Users can now toggle mqtt-io compatibility mode from addon UI.
Default true maintains backward compatibility for migrations. 
- fix(config): add legacy_mqttio compatibility settings

Add client_id and legacy_mqttio: true to all gpio2mqtt configs
for seamless migration from mqtt-io without entity duplication
in Home Assistant. 
- Merge pull request #53 from jethome-hassio-addons/feature/gpio2mqtt-dispatch-trigger

feat(ci): add gpio2mqtt dispatch trigger workflow 
- fix(ci): address security review comments

- Use env variables instead of direct payload interpolation to prevent
  script injection vulnerability
- Add comment explaining is_release/is_prerelease precedence logic 
- Update .github/workflows/gpio2mqtt-trigger.yaml

Co-authored-by: Copilot <175728472+Copilot@users.noreply.github.com> 
- feat(ci): add gpio2mqtt dispatch trigger workflow

- Add gpio2mqtt-trigger.yaml to handle repository_dispatch events
  from gpio2mqtt repository
- Update deploy.yaml to trigger on gpio2mqtt Trigger workflow completion
- Creates draft release for stable releases
- Creates draft prerelease for beta releases
- Dev builds only update edge channel 
- Merge pull request #52 from jethome-hassio-addons/feat/migrate-to-gpio2mqtt

feat: migrate from mqtt-io to gpio2mqtt 
- fix: quote on/off values in jethub-d1.yaml 
- fix: resolve CI linting errors

- Quote on/off values in YAML configs (truthy rule)
- Add hadolint ignore for DL3008 and DL3003
- Shorten long comment line in jethub-d1.yaml 
- fix: address BugBot review comments

- Fix oras download to use host architecture (dpkg --print-architecture)
  for cross-compilation support on aarch64
- Add missing `default: off` for relays in jethub-d1.yaml config 
- Prettified Code! 
- fix: resolve CI linting issues

- Add YAML document start marker (---) to all config files
- Add shellcheck disable directive for SC1091 
- fix: update Dockerfile to fetch binary from GHCR via ORAS

- Use multi-stage build: download binary in first stage via oras
- Add BINARY_VERSION arg (default: dev) to build.yaml
- Keep original addon name and description in config.yaml
- Fix maintainer email to dev@jethome.com 
- Prettified Code! 
- feat: migrate from mqtt-io to gpio2mqtt

Major update that replaces Python mqtt-io with Rust gpio2mqtt binary.

Changes:
- Replace Python mqtt-io with pre-built gpio2mqtt Rust binary
- Switch base image from Alpine+Python to Debian bookworm-slim
- Add amd64 architecture support
- Add support for JetHub D2 and H1 models (in addition to D1)
- Add module config variants with ZigBee/UXM control pins
- Replace s6-overlay with simple entrypoint.sh
- Add auto-detection via Supervisor API and devicetree
- Add new options: use_module_config, custom_config, mqtt.keepalive, mqtt.qos
- Update minimum Home Assistant version to 2024.1.0

Backward compatibility:
- Keep slug jethub-mqtt-io for existing users
- Keep default topic_prefix and client_id as jethub-mqtt-io
- MQTT topic structure and entity names unchanged 
