# Europe Configuration Index

This directory contains Deye inverter configurations for European grid standards.

## Countries/Regions Available

- Germany (VDE-AR-N 4105)
- Netherlands (RfG, NC RfG)
- Belgium (C10/11)
- Austria (TOR Erzeuger)
- France (Grid Code)
- United Kingdom (G98/G99)
- Spain (Grid Code)
- Italy (CEI 0-21)

## Common European Standards

- **VDE-AR-N 4105**: German grid connection standard
- **EN 50549**: European standard for grid connection
- **RfG (EU 2016/631)**: Requirements for Generators regulation

## File Naming Convention

Files are named using the format: `[InverterModel]-[Country]-[GridOperator]-[Standard]-[SetupMode].md`

Examples:

- `SUN-12K-SG04LP3-EU-Netherlands-Netbeheer-VDE4105-AC-Solar.md`
- `SUN-5K-G03-Germany-VDE-AR-N-4105-Basic.md`
- `SUN-8K-G03-P-UK-DNO-G98-SmartLoad.md`

### Naming Components

- **InverterModel**: SUN-12K-SG04LP3-EU, SUN-5K-G03, SUN-8K-G03-P, etc.
- **Country**: Netherlands, Germany, UK, etc.
- **GridOperator**: Netbeheer, VDE, DNO, etc. (or "GridStandard" for general)
- **Standard**: VDE4105, AR-N-4105, G98, RfG, etc.
- **SetupMode**: Basic, Generator, Smart-Load, AC-Couple, AC-Solar

**Note**: Inverter model comes first as it's the primary determinant of parameter compatibility and available features.

## Setup Modes

Different physical configurations require different inverter settings. See [Setup Modes Documentation](../../docs/setup-modes.md) for detailed explanations.

### Available Setup Modes

- **Basic**: Standard solar + battery + backup loads (most common)
- **Generator**: Basic setup + backup generator on GEN port
- **Smart-Load**: Basic setup + controllable loads on GEN port
- **AC-Couple**: Basic setup + AC-coupled solar on GEN port
- **AC-Solar**: Battery + AC-coupled solar only (no DC PV)

## Quick Reference

| Country | Standard | Voltage | Frequency | Setup Modes | Available Configurations |
|---------|----------|---------|-----------|-------------|-------------------------|
| Germany | VDE-AR-N 4105 | 230V ±10% | 50Hz ±0.2Hz | All modes supported | [Need contributions] |
| Netherlands | VDE4105/RfG | 220V/380V | 50Hz ±1.5Hz | All modes supported | [SUN-12K-SG04LP3-EU-AC-Solar](SUN-12K-SG04LP3-EU-Netherlands-Netbeheer-VDE4105-AC-Solar.md) |
| UK | G98/G99 | 230V ±10% | 50Hz ±1% | Grid-tie modes | [Need contributions] |

### Setup Mode Compatibility

- **Basic Setup**: Supported by all European grid standards
- **Generator Setup**: Check local regulations for generator connection requirements
- **Smart-Load Setup**: Verify load control compliance with grid operator
- **AC-Couple Setup**: Ensure AC-coupled inverters meet grid code requirements
- **AC-Solar Setup**: Limited backup capability, grid-dependent operation

### Inverter Model Considerations

Different Deye inverter models have varying:

- **Parameter Names**: Settings may be labeled differently
- **Value Ranges**: Protection limits and operational ranges vary
- **Available Features**: Not all models support all advanced functions
- **Firmware Differences**: Capabilities may change between firmware versions

**Important**: Always use the configuration specific to your exact inverter model and verify parameter compatibility.
