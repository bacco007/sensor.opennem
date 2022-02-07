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

[![Open your Home Assistant instance and start setting up a new integration.](https://my.home-assistant.io/badges/config_flow_start.svg)](https://my.home-assistant.io/redirect/config_flow_start/?domain=opennem)

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

Not all energy sources are applicable in each region, the sensor will only report the sources that are applicable to each region

| Name                             | Type            |                       | Attribute                                                  | Description        |
| -------------------------------- | --------------- | --------------------- | ---------------------------------------------------------- | ------------------ |
| Battery - Charging               | Load            | `battery_charging`    |                                                            |
| Battery - Discharging            | Energy Source   | `battery_discharging` |                                                            |
| BioEnergy (Biomass)              | Energy Source   | `bioenergy_biomass`   |                                                            |
| BioEnergy (Biogas)               | Energy Source   | `bioenergy_biogas`    |                                                            |
| Black Coal                       | Energy Source   | `coal_black`          |                                                            |
| Brown Coal                       | Energy Source   | `coal_brown`          |                                                            |
| Exported Electricity             | Outward Energy  | `exports`             | Electricity exported to other Regions                      |
| Demand                           | Demand          | `demand`              | Not Available in WA                                        |
| Distillate                       | Energy Source   | `distillate`          |                                                            |
| Emissions Factor                 | Emissions       | `emissions_factor`    | Tonnes of CO2 Equivalent per MW                            |
| Flow (between Regions)           | Energy Transfer | `flow_{region}`       | Energy Flow between interconnected regions                 |
| Generation by Fossil Fuels       | Calculated      | `fossilfuel`          | Electricity generated (in region) from Fossil Fuel sources |
| Generation by Renewables         | Calculated      | `renewables`          | Electricity generated (in region) from Renewable sources   |
| Generation vs Demand             | Calculated      | `genvsdemand`         | See Below (Not available in WA)                            |
| Gas (Combined Cycle Power Plant) | Energy Source   | `gas_ccgt`            |                                                            |
| Gas (Open Cycle Gas Turbines)    | Energy Source   | `gas_ocgt`            |                                                            |
| Gas (Reciprocating Engine)       | Energy Source   | `gas_recip`           |                                                            |
| Gas (Steam)                      | Energy Source   | `gas_steam`           |                                                            |
| Gas (Waste Coal Mine)            | Energy Source   | `gas_wcmg`            |                                                            |
| Electricity Generated            | Calculated      | `generation`          | Electricity generated in Region                            |
| Hydro                            | Energy Source   | `hydro`               |                                                            |
| Imported Electricity             | Incoming Energy | `imports`             | Electricity imported from other Regions                    |
| Spot Price                       | Price           |                       | `price`                                                    | Current Spot Price |
| Pumps                            | Load            |                       | `pumps`                                                    |                    |
| Solar (Rooftop)                  | Energy Source   | `solar_rooftop`       |                                                            |
| Solar (Utility)                  | Energy Source   | `solar_utility`       |                                                            |
| Temperature                      | Temperature     | `temperature`         | Current Average Temperature in Region                      |
| Wind                             | Energy Source   | `wind`                |

### Generation vs Demand

The `genvsdemand` attribute is a calculation of the generation in a region (excluding any imports) minus the the region's energy demands. Where the attribute is a negative number, the region is not generating sufficient energy to meet demand.

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
