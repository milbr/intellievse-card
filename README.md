# IntelliEVSE Card

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![GitHub Release](https://img.shields.io/github/v/release/milbr/intellievse-card)](https://github.com/milbr/intellievse-card/releases)
[![License](https://img.shields.io/github/license/milbr/intellievse-card)](LICENSE)

A custom Lovelace card for the [IntelliEVSE](https://github.com/milbr/intellievse) integration, providing real-time visualization and control of your intelligent EV charging system.

> **Note:** This card is currently in active development. Full HACS publication coming soon.

## Features

- Real-time price vs threshold visualization
- Current SOC and charging status display
- Percentile threshold controls with numeric inputs
- Boost controls for manual override
- Departure time scheduling
- Session cost and savings tracking

## Screenshot

*Coming soon*

## Installation

### HACS (Recommended)

1. Open HACS in Home Assistant
2. Click the three dots menu and select "Custom repositories"
3. Add `https://github.com/milbr/intellievse-card` as a Lovelace plugin
4. Search for "IntelliEVSE Card" and install
5. Add the resource to your Lovelace configuration

### Manual Installation

1. Download `intellievse-card.js` from the [latest release](https://github.com/milbr/intellievse-card/releases)
2. Copy it to your `www` folder
3. Add the resource to your Lovelace configuration:

```yaml
resources:
  - url: /local/intellievse-card.js
    type: module
```

## Configuration

### Basic Configuration

```yaml
type: custom:intellievse-card
price_sensor: sensor.comed_offset
soc_sensor: sensor.volvo_ex90_battery_charge_level
```

### Full Configuration

```yaml
type: custom:intellievse-card
price_sensor: sensor.comed_offset
soc_sensor: sensor.volvo_ex90_battery_charge_level
show_percentiles: true
```

### Options

| Option | Type | Description | Default |
|--------|------|-------------|---------|
| `price_sensor` | string | Entity ID for electricity price sensor | Required |
| `soc_sensor` | string | Entity ID for vehicle SOC sensor | Required |
| `show_percentiles` | boolean | Show percentile threshold controls | `true` |

## Requirements

- Home Assistant 2024.1 or newer
- [IntelliEVSE Integration](https://github.com/milbr/intellievse) installed and configured

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
