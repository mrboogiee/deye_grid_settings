# Asia-Pacific Configuration Index

This directory contains Deye inverter configurations for Asia-Pacific grid standards.

## Countries/Regions Available

- Australia (AS/NZS 4777.2)
- New Zealand (AS/NZS 4777.2)
- Japan (Grid Codes)
- Philippines (Grid Code)
- Thailand (Grid Code)

## Common Standards

- **AS/NZS 4777.2**: Australian/New Zealand grid connection standard
- **JIS C 8961**: Japanese grid-tie inverter standard
- Various national grid codes across APAC region

## File Naming Convention

Files are named using the format: `[InverterModel]-[Country]-[GridOperator]-[Standard]-[SetupMode].md`

Examples:

- `SUN-8K-G03-P-Australia-AEMO-AS4777-Basic.md`
- `SUN-12K-SG04LP3-AU-NewZealand-Transpower-AS4777-Generator.md`
- `SUN-5K-G03-Japan-TEPCO-JIS-SmartLoad.md`

### Naming Components

- **Country**: Australia, NewZealand, Japan, etc.
- **GridOperator**: AEMO, Transpower, TEPCO, etc.
- **Standard**: AS4777, JIS, national grid codes
- **SetupMode**: Basic, Generator, Smart-Load, AC-Couple, AC-Solar
- **InverterModel**: Model with regional suffix (AU, NZ, JP, etc.)

**Note**: APAC region models may have different voltage/frequency ratings and grid compliance features.

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
| Australia | AS/NZS 4777.2 | 230V ±10% | 50Hz ±1% | All modes supported | [Basic] [Smart-Load] |
| New Zealand | AS/NZS 4777.2 | 230V ±6% | 50Hz ±1% | All modes supported | [Basic] [Generator] |
| Japan | JIS C 8961 | 101V/202V | 50/60Hz ±0.2Hz | Grid-tie modes | [Basic] [AC-Couple] |

### Regional Considerations

- **Australia**: Dynamic export limiting and demand response capabilities
- **New Zealand**: Earthquake resilience and grid support requirements
- **Japan**: Dual frequency regions (50Hz/60Hz) require specific configurations
- **Southeast Asia**: High humidity and temperature considerations

### Setup Mode Compatibility

- **Basic Setup**: Supported across all APAC regions
- **Generator Setup**: Check local safety standards and connection requirements
- **Smart-Load Setup**: Ideal for demand management and peak shaving
- **AC-Couple Setup**: Common for retrofitting existing solar installations
- **AC-Solar Setup**: Grid-dependent operation, limited backup functionality

Note: Add entries as configurations are contributed
