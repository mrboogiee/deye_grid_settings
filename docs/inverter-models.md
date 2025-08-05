# Deye Inverter Models Reference

This document provides an overview of Deye inverter models and their capabilities. **Each model has specific parameter names, value ranges, and features that require model-specific configurations.**

## Why Model-Specific Configurations Matter

Different Deye inverter models have:

- **Different Parameter Names**: Settings may be labeled differently between models
- **Varying Value Ranges**: Protection limits and operational ranges change by model
- **Unique Features**: Not all models support the same advanced functions
- **Firmware Variations**: Capabilities and interfaces evolve with firmware updates
- **Regional Variants**: Same base model may have different capabilities by region

**Important**: Always use configurations specifically created for your exact inverter model and firmware version.

## Single Phase Models

| Model      | Power Rating | Features    | Grid Standards     |
| ---------- | ------------ | ----------- | ------------------ |
| SUN-3K-G03 | 3kW          | WiFi, RS485 | VDE-AR-N 4105, G98 |
| SUN-5K-G03 | 5kW          | WiFi, RS485 | VDE-AR-N 4105, G98 |
| SUN-6K-G03 | 6kW          | WiFi, RS485 | VDE-AR-N 4105, G98 |

## Three Phase Models

| Model         | Power Rating | Features             | Grid Standards     |
| ------------- | ------------ | -------------------- | ------------------ |
| SUN-5K-G03-P  | 5kW          | WiFi, RS485, 3-phase | VDE-AR-N 4105, G99 |
| SUN-8K-G03-P  | 8kW          | WiFi, RS485, 3-phase | VDE-AR-N 4105, G99 |
| SUN-12K-G03-P | 12kW         | WiFi, RS485, 3-phase | VDE-AR-N 4105, G99 |

## Hybrid Models (with Battery)

| Model           | Power Rating | Battery Support | Features     |
| --------------- | ------------ | --------------- | ------------ |
| SUN-5K-SG03LP1  | 5kW          | 48V lithium     | Backup, WiFi |
| SUN-8K-SG03LP1  | 8kW          | 48V lithium     | Backup, WiFi |
| SUN-12K-SG03LP1 | 12kW         | 48V lithium     | Backup, WiFi |

## Firmware Compatibility

Different firmware versions may have different parameter names or available settings. Always check the firmware version when using configurations.

Common firmware versions:

- v1.50.x: Early release
- v1.60.x: Enhanced grid support
- v1.70.x: Latest features

## Model Selection Guide

1. **Single Phase**: For residential installations up to 6kW
2. **Three Phase**: For larger residential or commercial installations
3. **Hybrid**: When battery backup is required

## Configuration Notes

- Some models may require specific settings for certain grid codes
- Hybrid models have additional battery-related parameters
- Check local regulations for maximum allowed power output
