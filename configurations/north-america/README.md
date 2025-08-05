# North America Configuration Index

This directory contains Deye inverter configurations for North American grid standards.

## Countries/Regions Available

- United States (IEEE 1547)
- Canada (CSA C22.2 No. 107.1)

## Common Standards

- **IEEE 1547**: US standard for interconnecting distributed resources
- **UL 1741**: US safety standard for inverters and converters
- **CSA C22.2 No. 107.1**: Canadian standard for power converters

## File Naming Convention

Files are named using the format: `[InverterModel]-[Country]-[GridOperator]-[Standard]-[SetupMode].md`

Examples:

- `SUN-12K-SG04LP3-US-USA-Utility-IEEE1547-Basic.md`
- `SUN-8K-G03-P-Canada-Hydro-CSA-Generator.md`
- `SUN-5K-G03-USA-PGE-IEEE1547-SmartLoad.md`

### Naming Components

- **Country**: USA, Canada
- **GridOperator**: Utility name or "GridStandard" for general
- **Standard**: IEEE1547, CSA, UL1741, etc.
- **SetupMode**: Basic, Generator, Smart-Load, AC-Couple, AC-Solar
- **InverterModel**: SUN-12K-SG04LP3-US, SUN-5K-G03, etc.

**Note**: Each inverter model may have different parameters and capabilities specific to North American grid requirements.

## Setup Modes

Different physical configurations require different inverter settings. See [Setup Modes Documentation](../../docs/setup-modes.md) for detailed explanations.

### Available Setup Modes

- **Basic**: Standard solar + battery + backup loads (most common)
- **Generator**: Basic setup + backup generator on GEN port
- **Smart-Load**: Basic setup + controllable loads on GEN port
- **AC-Couple**: Basic setup + AC-coupled solar on GEN port
- **AC-Solar**: Battery + AC-coupled solar only (no DC PV)

## Quick Reference

| Country | Standard | Voltage | Frequency | Setup Modes | Example Files |
|---------|----------|---------|-----------|-------------|---------------|
| USA | IEEE 1547 | 240V split-phase | 60Hz ±0.05Hz | All modes supported | [Basic] [Generator] |
| Canada | CSA C22.2 | 240V split-phase | 60Hz ±0.1Hz | All modes supported | [Basic] [Smart-Load] |

### Setup Mode Considerations

- **Basic Setup**: Standard residential installation, widely supported
- **Generator Setup**: Verify local electrical codes for generator connections
- **Smart-Load Setup**: Check utility demand response program compatibility
- **AC-Couple Setup**: Ensure rapid shutdown compliance (NEC 690.12)
- **AC-Solar Setup**: Limited backup capability during outages

Note: Add entries as configurations are contributed
