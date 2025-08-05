# Other Regions Configuration Index

This directory contains Deye inverter configurations for regions not covered in the main geographical categories.

## Regions Available

- Africa (Various national grid codes)
- Middle East (Regional standards)
- South America (National grid requirements)
- Caribbean (Island grid systems)
- Other territories and special cases

## File Naming Convention

Files are named using the format: `[InverterModel]-[Country]-[GridOperator]-[Standard]-[SetupMode].md`

Examples:

- `SUN-8K-G03-SouthAfrica-Eskom-NRS097-Basic.md`
- `SUN-12K-SG04LP3-BR-Brazil-ONS-GridCode-Generator.md`
- `SUN-5K-G03-UAE-DEWA-GridCode-SmartLoad.md`

### Naming Components

- **Country**: SouthAfrica, Brazil, UAE, etc.
- **GridOperator**: Eskom, ONS, DEWA, etc.
- **Standard**: Local grid codes and standards
- **SetupMode**: Basic, Generator, Smart-Load, AC-Couple, AC-Solar
- **InverterModel**: Model with regional designation if applicable

**Note**: Different regions may require specific inverter models or firmware versions for local compliance.

## Setup Modes

Different physical configurations require different inverter settings. See [Setup Modes Documentation](../../docs/setup-modes.md) for detailed explanations.

### Available Setup Modes

- **Basic**: Standard solar + battery + backup loads (most common)
- **Generator**: Basic setup + backup generator on GEN port
- **Smart-Load**: Basic setup + controllable loads on GEN port
- **AC-Couple**: Basic setup + AC-coupled solar on GEN port
- **AC-Solar**: Battery + AC-coupled solar only (no DC PV)

## Regional Considerations

### Grid Stability

Many regions have less stable grid infrastructure, making certain setup modes more suitable:

- **Generator Setup**: Essential in areas with frequent outages
- **Basic Setup**: Provides reliable backup during grid instability
- **Smart-Load Setup**: Helps manage demand during peak periods

### Climate Factors

- **High Temperature**: May require derating and enhanced cooling
- **High Humidity**: Additional protection against corrosion
- **Extreme Weather**: Enhanced mechanical protection requirements

### Economic Factors

- **Limited Grid Access**: Generator and battery backup become critical
- **Variable Tariffs**: Smart-load management for cost optimization
- **Fuel Availability**: Generator setup considerations

## Setup Mode Recommendations by Region Type

| Region Type | Primary Setup | Secondary Setup | Key Benefits |
|-------------|---------------|-----------------|--------------|
| Island Grids | Generator | Basic | Extended backup, grid support |
| Developing Infrastructure | Basic | Generator | Reliability, cost-effective |
| Industrial Zones | Smart-Load | AC-Couple | Demand management, expansion |
| Remote Areas | Generator | Basic | Energy independence |

Note: Always verify local regulations and grid operator requirements before implementation
