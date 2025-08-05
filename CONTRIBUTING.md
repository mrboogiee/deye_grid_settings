
# Contributing to Deye Grid Settings

Thank you for your interest in contributing to the Deye Grid Settings documentation! This repository aims to provide a comprehensive collection of Deye inverter settings for different grid scenarios and configurations.

## Commercial Use Guidelines

We welcome use by commercial integrators, but ask that:

- You contribute back improvements or customizations where possible
- You **do not** repackage or resell these configurations without attribution
- You give credit to the original authors in public distributions

## How to Contribute

### 1. Types of Contributions

We welcome the following types of contributions:

- **New grid configuration settings** for different regions/countries/setup modes
- **Setup mode documentation** for different physical configurations
- **Documentation improvements** for existing configurations
- **Bug fixes** in existing settings or documentation
- **Testing results** and validation of existing configurations
- **Translation** of documentation to other languages

### 2. Before Contributing

- Check existing issues and pull requests to avoid duplicates
- Review [Setup Modes Documentation](docs/setup-modes.md) to understand physical configurations
- Test your configurations thoroughly before submitting
- Ensure your settings comply with local grid codes and regulations
- Document the specific inverter model(s) and setup mode your settings apply to

### 3. Submission Process

1. **Fork** this repository
2. **Create a new branch** for your contribution: `git checkout -b feature/your-contribution-name`
3. **Add your configuration** following the established format
4. **Test** your settings (if possible) and document the results
5. **Commit** your changes with clear, descriptive commit messages
6. **Submit a pull request** with a detailed description

### 4. Configuration Documentation Standards

When submitting new configurations, please include:

#### Required Information

- **Country/Region**: Where these settings are applicable
- **Grid operator**: Specific utility company (if applicable)
- **Setup mode**: Physical configuration (Basic/Generator/Smart-Load/AC-Couple/AC-Solar)
- **Inverter model**: Specific Deye model (e.g., SUN-12K-SG04LP3-EU)
- **Grid standards**: Relevant grid codes (e.g., VDE-AR-N 4105, IEEE 1547, etc.)
- **Date tested**: When these settings were last verified
- **Firmware version**: Inverter firmware version used

#### Configuration Format

```text
# [InverterModel] - [Country/Region] - [Grid Operator] - [Grid Standard] - [Setup Mode]

## Setup Mode
Physical configuration and connection summary

## Inverter Model
Specific model information and firmware details

## Settings
Parameter Name: Value
Parameter Name: Value

## Setup-Specific Settings
(Generator control, load management, AC-coupling, etc.)

## Notes
- Any special considerations
- Known limitations
- Setup mode requirements
- Model-specific considerations
```

#### Optional but Helpful

- Screenshots of inverter configuration screens
- Test results or certification documents (if shareable)
- Contact information for verification questions

### 5. Quality Guidelines

- **Accuracy**: Ensure all settings are correct and have been tested
- **Clarity**: Use clear, descriptive naming for files and parameters
- **Completeness**: Include all necessary parameters for a working configuration
- **Safety**: Only submit settings that comply with local safety regulations

### 6. Review Process

All contributions will be reviewed by maintainers to ensure:

- Technical accuracy
- Compliance with safety standards
- Proper documentation format
- No conflicts with existing configurations

## Getting Help

If you need help with contributing:

- Open an issue with your question
- Check existing documentation and issues first
- Be specific about your inverter model and grid requirements

## Code of Conduct

- Be respectful and constructive in all communications
- Focus on helping others succeed with their installations
- Share knowledge openly while respecting intellectual property
- Prioritize safety and compliance in all contributions

## License

By contributing to this repository, you agree that your contributions will be licensed under the same license as the project (GPL-3.0).

---

**Important Safety Note**: Always consult with qualified electrical professionals and ensure compliance with local grid codes before implementing any settings. The contributors and maintainers of this repository are not responsible for any damage or non-compliance resulting from the use of these configurations.
