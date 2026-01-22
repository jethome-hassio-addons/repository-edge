# Changelog since v0.3.0
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
