# sensor.opennem

## Home Assistant sensor for OpenNEM Data

[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]][license]

[![hacs][hacsbadge]][hacs]
[![Project Maintenance][maintenance-shield]][user_profile]
[![BuyMeCoffee][buymecoffeebadge]][buymecoffee]

[![Community Forum][forum-shield]][forum]

_This component will set up a sensor platform to retrieve data from [OpenNEM](http://www.opennem.org.au), an open platform to access [National Electricity Market](https://www.aemo.com.au/energy-systems/electricity/national-electricity-market-nem/about-the-national-electricity-market-nem) Data (Australia)_

**This component will set up the following platforms.**

| Platform | Description                 |
| -------- | --------------------------- |
| `sensor` | Show info from OpenNEM API. |

## Installation

### Manual Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `opennem`.
4. Download _all_ the files from the `custom_components/opennem/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Create Configuration (see below)
7. Restart Home Assistant
8. In the HA UI go to "Configuration" -> "Integrations" click "+" and search for "OpenNEM"

### Installation via Home Assistant Community Store (HACS)

1. Ensure [HACS](http://hacs.xyz/) is installed.
2. Search for and install the "OpenNEM (AU) Data" integration
3. Configure the sensor
4. Restart Home Assistant
5. In the HA UI go to "Configuration" -> "Integrations" click "+" and search for "OpenNEM"

## Configuration is done in the UI

<!---->

## Regions

OpenNEM data is published for the following regions (states):

| State                  | Region for Config |
| ---------------------- | ----------------- |
| Queensland             | qld               |
| New South Wales        | nsw               |
| Victoria               | vic               |
| South Australia        | sa                |
| Tasmania               | tas               |
| Western Australia      | wa                |
| National Energy Market | nem               |

## Attributes

| Type                             | Attribute             | Description                                                |
| -------------------------------- | --------------------- | ---------------------------------------------------------- |
| Battery - Charging               | `battery_charging`    |                                                            |
| Battery - Discharging            | `battery_discharging` |                                                            |
| BioEnergy (Biomass)              | `bioenergy_biomass`   |                                                            |
| BioEnergy (Biogas)               | `bioenergy_biogas`    |                                                            |
| Black Coal                       | `coal_black`          |                                                            |
| Brown Coal                       | `coal_brown`          |                                                            |
| Exported Electricity             | `exports`             | Electricity exported to other Regions                      |
| Demand                           | `demand`              |                                                            |
| Distillate                       | `distillate`          |                                                            |
| Generation by Fossil Fuels       | `fossilfuel`          | Electricity generated (in region) from Fossil Fuel sources |
| Generation by Renewables         | `renewables`          | Electricity generated (in region) from Renewable sources   |
| Gas (Combined Cycle Power Plant) | `gas_ccgt`            |                                                            |
| Gas (Open Cycle Gas Turbines)    | `gas_ocgt`            |                                                            |
| Gas (Reciprocating Engine)       | `gas_recip`           |                                                            |
| Gas (Steam)                      | `gas_steam`           |                                                            |
| Gas (Waste Coal Mine)            | `gas_wcmg`            |                                                            |
| Electricity Generated            | `generation`          | Electricity generated in Region                            |
| Hydro                            | `hydro`               |                                                            |
| Imported Electricity             | `imports`             | Electricity imported from other Regions                    |
| Spot Price                       | `price`               | Current Spot Price                                         |
| Pumps                            | `pumps`               |                                                            |
| Solar (Rooftop)                  | `solar_rooftop`       |                                                            |
| Solar (Utility)                  | `solar_utility`       |                                                            |
| Temperature                      | `temperature`         | Current Average Temperature in Region                      |
| Wind                             | `wind`                |

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)

---

[integration_blueprint]: https://github.com/bacco007/sensor.opennem
[buymecoffee]: https://www.buymeacoffee.com/bacco007
[buymecoffeebadge]: https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg?style=for-the-badge
[commits-shield]: https://img.shields.io/github/commit-activity/y/bacco007/sensor.opennem.svg?style=for-the-badge
[commits]: https://github.com/bacco007/sensor.opennem/commits/master
[hacs]: https://hacs.xyz
[hacsbadge]: https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge
[discord]: https://discord.gg/Qa5fW2R
[discord-shield]: https://img.shields.io/discord/330944238910963714.svg?style=for-the-badge
[exampleimg]: example.png
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg?style=for-the-badge
[forum]: https://community.home-assistant.io/t/custom-component-australia-opennem/168239
[license]: https://github.com/bacco007/sensor.opennem/blob/main/LICENSE
[license-shield]: https://img.shields.io/github/license/bacco007/sensor.opennem.svg?style=for-the-badge
[maintenance-shield]: https://img.shields.io/badge/maintainer-Thomas%20Baxter%20%40bacco007-blue.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/bacco007/sensor.opennem.svg?style=for-the-badge
[releases]: https://github.com/bacco007/sensor.opennem/releases
[user_profile]: https://github.com/bacco007
