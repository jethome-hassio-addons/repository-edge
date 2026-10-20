- feat: JetHub D3-mini (J310) support

- jethub-d3.yaml: UXM1-4 RESET/MODE switches on TCA6408A I2C expander
- entrypoint: auto-resolve expander gpiochip via sysfs (i2c client tca6408),
  GPIO2MQTT_TCA6408_CHIP override for testing; module-config fallback
- detect-model: compatible s7_s905y5_j310, board j310, D3-mini model string
- docs: D3 device notes (RGB LED is kernel gpio-leds managed, not exposed)
