- fix: legacy guard must not trust a 404 from /addons/{slug}/info

That endpoint resolves through store data on some Supervisor versions and
can 404 for an installed add-on (seen on a live D2: 404 while the GPIO
lines were busy). The installed-apps list from GET /supervisor/info is
now the primary source; the legacy add-on is matched by slug OR name
(covers differently-slugged installs), ourselves excluded. The guard
also logs the slug=state digest of installed apps for self-diagnosis.
