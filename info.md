# IntelliEVSE Card

A custom Lovelace card for the [IntelliEVSE](https://github.com/milbr/intellievse) integration.

## Features

- Real-time price vs threshold visualization
- Current SOC and charging status display
- Percentile threshold controls
- Boost controls for manual override
- Departure time scheduling
- Session cost and savings tracking

## Requirements

- [IntelliEVSE Integration](https://github.com/milbr/intellievse) installed and configured

## Card Configuration

```yaml
type: custom:intellievse-card
price_sensor: sensor.your_price_sensor
soc_sensor: sensor.your_soc_sensor
show_percentiles: true
```

| Option | Description | Default |
|--------|-------------|---------|
| `price_sensor` | Entity ID for electricity price | Required |
| `soc_sensor` | Entity ID for vehicle SOC | Required |
| `show_percentiles` | Show percentile controls | `true` |
