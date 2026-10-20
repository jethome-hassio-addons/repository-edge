- feat: refuse to start while legacy jethub-mqtt-io addon is running

Startup guard via Supervisor API /info; fail-open when the API or token
is unavailable. Replaces the manual 'do not run both' warning.
