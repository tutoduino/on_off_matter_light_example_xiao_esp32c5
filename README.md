# on_off_matter_light_example_xiao_esp32c5

A Matter over WiFi **on/off light** example for the [Seeed Studio XIAO ESP32C5](https://wiki.seeedstudio.com/xiao_esp32c5_getting_started/) module, based on the [esp-matter](https://github.com/espressif/esp-matter) SDK.

## Description

This example creates a Matter on/off light device using the ESP Matter data model. The onboard yellow LED (GPIO27, active low) is controlled via the Matter OnOff cluster, and can be integrated with Home Assistant or any Matter-compatible controller.

It is derived from the `light` example of esp-matter, simplified for a single GPIO LED (no RGB, no brightness control).

## Hardware

- Seeed Studio XIAO ESP32C5
- Onboard LED on GPIO27 (active low)
- Boot button on GPIO28

## Requirements

- [ESP-IDF v5.5](https://github.com/espressif/esp-idf)
- [esp-matter](https://github.com/espressif/esp-matter)

## Installation

This example must be placed in the `examples/` directory of esp-matter, at the same level as the `light` example:
```
esp-matter/
└── examples/
    ├── light/
    └── on_off_matter_light_example_xiao_esp32c5/   ← here
```

## Build and flash
```bash
idf.py fullclean
idf.py set-target esp32c5
idf.py build
idf.py flash monitor
```

## Matter integration

This example supports Matter over WiFi. After flashing, commission the device using a Matter-compatible app (e.g. Home Assistant, Apple Home, Google Home).

The onboard LED reflects the on/off state of the Matter endpoint.
