# SUN-12K-SG04LP3-EU - Netherlands - Netbeheer - VDE4105 - AC-Solar

[!WARNING] WORK IN PROGRESS, NOT CORRECT PER SE...

## Overview

This configuration is for the Deye SUN-12K-SG04LP3-EU hybrid inverter operating in AC-Solar setup mode in the Netherlands. This setup uses only AC-coupled solar (microinverters) connected to the GEN port, with no DC PV panels connected to the inverter's PV inputs.

## Setup Mode

**Physical Configuration**: AC-Solar

See [Setup Modes Documentation](../../docs/setup-modes.md) for detailed connection diagrams.

### Connection Summary

- ✅ Battery connected to battery port (300Ah BMS Lithium)
- ❌ PV panels NOT connected to PV inputs (pure AC-coupled system)
- ✅ Home loads connected to GRID-side
- ✅ Backup loads connected to LOAD port
- ✅ AC-coupled solar (microinverters) connected to GEN port

## Inverter Model

- **Deye SUN-12K-SG04LP3-EU** (12kW Three-Phase Hybrid Inverter)

## Grid Requirements

- **Grid Standard**: VDE-AR-N 4105 (German standard used in Netherlands)
- **Voltage Range**: LN: 220VAC, LL: 380VAC
- **Frequency Range**: 50Hz ±1.5Hz (47.5-51.5Hz normal operation)
- **Power Factor**: 1.0 (unity power factor)
- **Phase Type**: Three-phase (0° 240° 120°)

## Configuration Settings

### Battery Settings

| Parameter             | Value            | Unit | Description                   |
| --------------------- | ---------------- | ---- | ----------------------------- |
| Battery Type          | BMS Lithium Batt | -    | Lithium battery with BMS      |
| Battery Capacity      | 300              | Ah   | Total battery capacity        |
| Max Charge Current    | 240              | A    | Maximum charging current      |
| Max Discharge Current | 240              | A    | Maximum discharge current     |
| Battery Shutdown SOC  | 10               | %    | Low SOC cutoff point          |
| Battery Restart SOC   | 50               | %    | SOC to restart after shutdown |
| Battery Low Warning   | 15               | %    | Low battery warning level     |
| Grid Charge Enable    | Enable           | -    | Allow charging from grid      |
| Grid Start SOC        | 30               | %    | SOC to start grid charging    |
| Grid Charge Current   | 40               | A    | Grid charging current limit   |
| Battery Efficiency    | 99               | %    | Round-trip efficiency         |
| Battery Resistance    | 25               | mΩ   | Internal resistance           |

### System Work Mode Settings

| Parameter         | Value               | Unit | Description               |
| ----------------- | ------------------- | ---- | ------------------------- |
| System Work Mode  | Zero Export To Load | -    | Zero export operation     |
| Solar Sell        | Enable              | -    | Allow excess solar export |
| Setup Code        | 1111111             | -    | Configuration setup code  |
| Max Solar Power   | 12000               | W    | Maximum solar input power |
| Max Sell Power    | 12000               | W    | Maximum export power      |
| Energy Pattern    | Load First          | -    | Load priority mode        |
| Zero Export Power | 20                  | W    | Export threshold          |

### Time of Use Settings

| Parameter             | Value                                    | Unit | Description                       |
| --------------------- | ---------------------------------------- | ---- | --------------------------------- |
| Time of Use           | ON                                       | -    | TOU mode enabled                  |
| SOC2                  | 15                                       | %    | Secondary SOC threshold           |
| Time Slots            | 6                                        | -    | Number of time periods            |
| Time 1-6 Grid Charge  | ON                                       | -    | Grid charging enabled all periods |
| Selling Mode Times    | 01:00, 05:00, 09:00, 13:00, 17:00, 21:00 | -    | Time slot boundaries              |
| GPS Power (all slots) | 12000                                    | W    | Grid power limit per slot         |
| SOC1 (all slots)      | 20                                       | %    | Primary SOC threshold             |

### Grid Protection Settings

| Parameter                | Value | Unit | Description                       |
| ------------------------ | ----- | ---- | --------------------------------- |
| Grid V High (Normal)     | 287.5 | V    | High voltage trip (normal)        |
| Grid V Low (Normal)      | 103.5 | V    | Low voltage trip (normal)         |
| Grid Hz High (Normal)    | 51.5  | Hz   | High frequency trip (normal)      |
| Grid Hz Low (Normal)     | 47.5  | Hz   | Low frequency trip (normal)       |
| Grid V High (Reconnect)  | 251   | V    | High voltage reconnection limit   |
| Grid V Low (Reconnect)   | 186   | V    | Low voltage reconnection limit    |
| Grid Hz High (Reconnect) | 51.3  | Hz   | High frequency reconnection limit |
| Grid Hz Low (Reconnect)  | 47.7  | Hz   | Low frequency reconnection limit  |
| Grid Reconnection Time   | 60    | s    | Delay before reconnection         |
| Normal Ramp Rate         | 60    | s    | Power ramp rate (normal)          |
| Reconnect Ramp Rate      | 36    | s    | Power ramp rate (reconnect)       |

### Instant Protection Settings

| Parameter                 | Value | Unit | Description                     |
| ------------------------- | ----- | ---- | ------------------------------- |
| Over Voltage (10min mean) | 253   | V    | Long-term overvoltage limit     |
| U< 1 (Undervoltage 1)     | 184   | V    | First undervoltage threshold    |
| U< 1 Trip Delay           | 1     | s    | Delay for U< 1 trip             |
| U> 1 (Overvoltage 1)      | 253   | V    | First overvoltage threshold     |
| U> 1 Trip Delay           | 0.12  | s    | Delay for U> 1 trip             |
| U< 2 (Undervoltage 2)     | 103.5 | V    | Second undervoltage threshold   |
| U< 2 Trip Delay           | 0.2   | s    | Delay for U< 2 trip             |
| U> 2 (Overvoltage 2)      | 287.5 | V    | Second overvoltage threshold    |
| U> 2 Trip Delay           | 0.12  | s    | Delay for U> 2 trip             |
| F< 1 (Underfrequency 1)   | 47.5  | Hz   | First underfrequency threshold  |
| F< 1 Trip Delay           | 0.12  | s    | Delay for F< 1 trip             |
| F> 1 (Overfrequency 1)    | 51.5  | Hz   | First overfrequency threshold   |
| F> 1 Trip Delay           | 0.12  | s    | Delay for F> 1 trip             |
| F< 2 (Underfrequency 2)   | 47.5  | Hz   | Second underfrequency threshold |
| F< 2 Trip Delay           | 0.12  | s    | Delay for F< 2 trip             |
| F> 2 (Overfrequency 2)    | 51.5  | Hz   | Second overfrequency threshold  |
| F> 2 Trip Delay           | 0.12  | s    | Delay for F> 2 trip             |

### Frequency Response Settings

| Parameter     | Value                          | Unit   | Description                      |
| ------------- | ------------------------------ | ------ | -------------------------------- |
| F(W) Mode     | UnderFre Enable OverFre Enable | -      | Frequency-power response         |
| Drop F>       | 40                             | %PE/Hz | Power reduction rate (overfreq)  |
| Start Freq F> | 50.2                           | Hz     | Start frequency (overfreq)       |
| Stop Freq F>  | 50.2                           | Hz     | Stop frequency (overfreq)        |
| Drop F<       | 40                             | %PE/Hz | Power reduction rate (underfreq) |
| Start Freq F< | 49.8                           | Hz     | Start frequency (underfreq)      |
| Stop Freq F<  | 49.8                           | Hz     | Stop frequency (underfreq)       |

### Power Quality Settings

| Parameter          | Value   | Unit | Description                     |
| ------------------ | ------- | ---- | ------------------------------- |
| V(W)               | Disable | -    | Voltage-power response          |
| V(Q)               | Disable | -    | Voltage-reactive power response |
| P(Q)               | Disable | -    | Active-reactive power response  |
| P(F)               | Disable | -    | Power-frequency response        |
| P(U) Response Time | 3       | s    | Voltage response time constant  |
| Q(U) Response Time | 0.1     | s    | Reactive power response time    |
| Minimum Cos Phi    | 0.85    | -    | Minimum power factor            |
| Fixed Q            | 0       | %    | Fixed reactive power            |

### AC-Solar Specific Settings

| Parameter                | Value        | Unit | Description                      |
| ------------------------ | ------------ | ---- | -------------------------------- |
| SmartLoad Setup          | MicInv Input | -    | AC microinverter input mode      |
| AC Couple OFF %          | 100          | %    | AC coupling disconnect threshold |
| AC Couple ON %           | 95           | %    | AC coupling reconnect threshold  |
| AC Couple on Grid Side   | Disable      | -    | Grid-side AC coupling            |
| AC Couple on Load Side   | Disable      | -    | Load-side AC coupling            |
| MI Export to Grid Cutoff | Disable      | -    | Microinverter export cutoff      |
| AC Couple Frequency High | 55           | Hz   | AC coupling frequency limit      |

### High/Low Voltage Ride Through

| Parameter | Value   | Unit | Description               |
| --------- | ------- | ---- | ------------------------- |
| HVRT      | Disable | -    | High voltage ride through |
| LVRT      | Disable | -    | Low voltage ride through  |
| Zero I    | Enable  | -    | Zero current injection    |
| HV1       | 115     | %    | High voltage level 1      |
| HV2       | 120     | %    | High voltage level 2      |
| HV3       | 125     | %    | High voltage level 3      |
| LV1       | 85      | %    | Low voltage level 1       |
| LV2       | 15      | %    | Low voltage level 2       |
| HV1 Time  | 60000   | ms   | HV1 trip time             |
| HV2 Time  | 5000    | ms   | HV2 trip time             |
| HV3 Time  | 100     | ms   | HV3 trip time             |
| LV1 Time  | 3000    | ms   | LV1 trip time             |
| LV2 Time  | 150     | ms   | LV2 trip time             |

### Advanced Functions

| Parameter                | Value   | Unit | Description                |
| ------------------------ | ------- | ---- | -------------------------- |
| ARC Setup                | OFF     | -    | Arc fault detection        |
| Grid Peak Shaving        | Disable | -    | Grid power limiting        |
| Grid Peak Shaving Power  | 12000   | W    | Grid power limit           |
| Signal Island Mode       | Enable  | -    | Anti-islanding protection  |
| Backup Delay             | 0       | s    | Backup switching delay     |
| CT Ratio                 | 2000:1  | -    | Current transformer ratio  |
| Asymmetric Phase Feeding | Enable  | -    | Unbalanced phase operation |
| Equipment Mode           | Slave   | -    | Parallel operation mode    |
| Modbus SN                | 1       | -    | Modbus address             |

## Installation Notes

### AC-Solar Setup Requirements

- **No DC PV panels**: All solar generation comes from AC-coupled microinverters
- **Microinverter connection**: Connect AC-coupled solar to GEN port
- **Grid dependency**: AC-coupled solar only available during grid connection
- **Backup limitation**: No solar charging during grid outages
- **Frequency regulation**: Microinverters controlled via frequency modulation

### Netherlands Grid Compliance

- VDE-AR-N 4105 standard applied (commonly used in Netherlands)
- Zero export configuration for net metering compliance
- Time-of-use optimization enabled for variable tariffs
- Asymmetric phase feeding enabled for three-phase installations

### Safety Considerations

- Proper isolation between AC-coupled solar and backup circuits
- Grid-tie protection settings comply with Dutch grid codes
- Anti-islanding protection enabled
- Current transformer ratio set for 2000:1 monitoring

## Testing Results

- **Date Tested**: WIP
- **Test Duration**: WIP
- **Grid Standard**: VDE4105
- **AC-Solar Operation**: WIP
- **Zero Export**: WIP

## Known Issues

- AC-coupled solar not available during grid outages (by design)
- Limited backup solar generation capability
- Dependency on grid for AC-coupled solar production
- Frequency regulation may conflict with some microinverter brands

## Contact Information

- **Configuration Date**: 2025-08-04
- **Firmware Compatibility**: SUN-12K-SG04LP3-EU series
- **Grid Standard**: VDE-AR-N 4105 (Netherlands implementation)
- **Setup Mode**: AC-Solar (microinverters only)

---

*Always verify settings with local grid operator and qualified electrical professionals before implementation. This configuration is specific to the SUN-12K-SG04LP3-EU model and may not be suitable for other inverter models.*
