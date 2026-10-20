- feat: align wrapper with gpio2mqtt 0.2.0

- bundled configs: short entity names (HA has_entity_name adds the
  device-name prefix; old names produced 'JetHub D1 JetHub Relay 1')
- new restore_mode option (off|on|restore, default restore) applied to
  every output without its own restore_mode/restore_state
- detect-model: actionable hint for Supervised installs (qemuarm-64,
  no device tree in container)
- DOCS: restore behavior section
