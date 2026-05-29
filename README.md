# docker-voltronic-homeassistant (common)

> **Note:** This repository is not used on its own. It holds the shared inverter
> poller and MQTT bridge sources that the Home Assistant add-on consumes as a
> git submodule.
>
> To install or use the add-on, go to the main repository:
> **https://github.com/m-byte/voltronic-homeassistant**

## What's in here

The buildable shared code under `sources/`:

- `inverter-cli/` — the C++ `inverter_poller` that reads the inverter over serial/USB.
- `inverter-mqtt/` — the MQTT publish/subscribe and Home Assistant discovery scripts.

The add-on variants in the main repository reference this repo as a submodule and build it.
