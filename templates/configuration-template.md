# [InverterModel] - [Country/Region] - [Grid Operator] - [Grid Standard] - [Setup Mode]

## Overview

Brief description of the grid requirements and specific use case for this setup mode and inverter model.

## Setup Mode

**Physical Configuration**: [Basic/Generator/Smart-Load/AC-Couple/AC-Solar]

See [Setup Modes Documentation](../docs/setup-modes.md) for detailed connection diagrams.

### Connection Summary

- ✅/❌ Battery connected to battery port
- ✅/❌ PV panels connected to PV inputs (PV1/PV2)
- ✅/❌ Home loads connected to GRID-side
- ✅/❌ Backup loads connected to LOAD port
- ✅/❌ [Generator/Smart-Load/AC-Solar] connected to GEN port

## Inverter Model

- **Deye [Model]** (e.g., SUN-12K-SG04LP3-EU - 12kW Three-Phase Hybrid)
- **Firmware Version**: [Version tested with these settings]
- **Model Notes**: Any specific considerations for this model

## Grid Requirements

- **Grid Standard**: (e.g., VDE-AR-N 4105, IEEE 1547, AS/NZS 4777.2)
- **Voltage Range**: (e.g., 220V-240V ±10%)
- **Frequency Range**: (e.g., 50Hz ±1%)
- **Power Factor**: (e.g., 0.9 leading to 0.9 lagging)

## Configuration Settings

### Grid Protection Settings

| Parameter                  | Value | Unit | Description                  |
| -------------------------- | ----- | ---- | ---------------------------- |
| Over Voltage Protection 1  | xxx   | V    | High voltage trip point      |
| Over Voltage Protection 2  | xxx   | V    | Very high voltage trip point |
| Under Voltage Protection 1 | xxx   | V    | Low voltage trip point       |
| Under Voltage Protection 2 | xxx   | V    | Very low voltage trip point  |
| Over Frequency Protection  | xxx   | Hz   | High frequency trip point    |
| Under Frequency Protection | xxx   | Hz   | Low frequency trip point     |

### Power Quality Settings

| Parameter              | Value | Unit | Description            |
| ---------------------- | ----- | ---- | ---------------------- |
| Power Factor           | xxx   | -    | Target power factor    |
| Reactive Power Control | xxx   | var  | Reactive power setting |
| Maximum Power          | xxx   | W    | Maximum output power   |

### Reconnection Settings

| Parameter          | Value | Unit | Description               |
| ------------------ | ----- | ---- | ------------------------- |
| Reconnection Delay | xxx   | s    | Delay before reconnection |
| Soft Start Time    | xxx   | s    | Gradual power ramp time   |

### Setup Mode Specific Settings

*Include settings specific to the chosen setup mode:*

**For Generator Setup:**

- Generator start/stop control settings
- Generator voltage/frequency parameters
- Automatic transfer switch timing

**For Smart-Load Setup:**

- Load control parameters
- Time-based scheduling settings
- Power threshold configurations

**For AC-Couple/AC-Solar Setup:**

- AC-coupled inverter frequency regulation
- Power coordination settings
- Backup operation parameters

## Installation Notes

- Any specific installation requirements for this setup mode
- Special considerations for this grid type and configuration
- Required external equipment (generators, smart loads, AC inverters)
- Safety isolation requirements between circuits

## Testing Results

- **Date Tested**: YYYY-MM-DD
- **Firmware Version**: x.x.x
- **Test Duration**: X hours/days
- **Test Results**: Summary of test outcomes

## Certification

- **Certification Body**: (if applicable)
- **Certificate Number**: (if applicable)
- **Valid Until**: (if applicable)

## Known Issues

- List any known limitations or issues
- Workarounds if available

## Contact Information

- **Contributor**: Name/Organization
- **Contact**: Email (optional)
- **Date Submitted**: YYYY-MM-DD

---
*Always verify settings with local grid operator and qualified electrical professionals before implementation.*
