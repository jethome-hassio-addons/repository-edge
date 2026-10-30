# Changelog since v1.0.2
- fix(unexport): resolve sysfs chip base on kernel 6.x and fail loudly

Issue #2 (JetHub D1+, Armbian 6.6, HA Supervised): all configured lines
were sysfs-held (left by the legacy sysfs-based addon) and the chardev
requests failed with EBUSY, while gpio-unexport.py silently unexported
nothing because none of its base-resolution methods matched the modern
sysfs topology.

- Method 1 now checks the resolved /sys/bus/gpio/devices/gpiochipN dir
  itself: on kernel 6.x the symlink points straight into the legacy chip
  directory which contains .
- Legacy parent/gpio/gpiochip* and major:minor methods kept as fallbacks.
- New label fallback: chardev chip label read via the GPIO uAPI ioctl,
  matched against /sys/class/gpio/gpiochip*/label.
- If the base is still unresolved while the sysfs interface is active:
  loud error listing the configured line offsets with a manual-unexport
  hint and a non-zero exit code instead of a silent zero. Quiet skip is
  kept for systems without the sysfs GPIO interface.

Tested against mocked sysfs topologies (6.x, legacy, no-sysfs,
unresolvable) and real gpiochips. 
