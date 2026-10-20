- fix: legacy-addon guard queried the wrong Supervisor endpoint

GET /info is the ROOT endpoint and carries no addons list, so the guard
silently concluded 'not installed'. Primary is now GET
/addons/jethub-mqtt-io/info (matches the /.+/info access pattern of the
default hassio role), with GET /supervisor/info (v1 payload with the
embedded addons array) as fallback. Every skip path now says why in the log.
