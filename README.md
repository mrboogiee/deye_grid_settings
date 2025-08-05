# Deye Grid Settings Repository

This is a work-in-progress repository for Deye inverter grid settings, focusing on configurations for different regions and setup modes. The goal is to provide a comprehensive resource for installers and users to ensure compliance with local grid codes and optimal performance and to make it easier to find back information regarding configurations.

A comprehensive repository documenting Deye inverter settings for different grid scenarios, countries, and electrical standards worldwide.

## 🎯 Purpose

This repository provides tested and verified grid connection settings for Deye solar inverters to ensure compliance with local grid codes and optimal performance across different regions.

## 📁 Repository Structure

```text
deye_grid_settings/
├── configurations/          # Grid settings by region
│   ├── europe/             # European grid standards
│   ├── north-america/      # US/Canada grid codes
│   ├── asia-pacific/       # APAC region settings
│   └── other-regions/      # Other countries/regions
├── templates/              # Configuration templates
├── docs/                   # Documentation and guides
├── testing/               # Test results and validation
└── CONTRIBUTING.md        # Contribution guidelines
```

## 🌍 Supported Regions

### Europe

- Germany (VDE-AR-N 4105)
- Netherlands (RfG, NC RfG)
- United Kingdom (G98/G99)
- And more European countries

### North America

- United States (IEEE 1547)
- Canada (CSA standards)

### Asia-Pacific

- Australia (AS/NZS 4777.2)
- New Zealand
- Various APAC countries

*More regions added regularly through community contributions*

## 🔧 Supported Inverter Models

This repository covers settings for various Deye inverter models including:

- **Single Phase**: SUN-3K-G03, SUN-5K-G03, SUN-6K-G03
- **Three Phase**: SUN-5K-G03-P, SUN-8K-G03-P, SUN-12K-G03-P  
- **Hybrid Models**: SUN-5K-SG03LP1, SUN-8K-SG03LP1, SUN-12K-SG03LP1

See [docs/inverter-models.md](docs/inverter-models.md) for complete model reference.

## 🚀 Quick Start

1. **Find your region**: Navigate to the appropriate folder in `configurations/`
2. **Choose your setup mode**: Review [Setup Modes](docs/setup-modes.md) to understand physical configurations
3. **Select your grid standard**: Choose the configuration file matching your local grid code and setup mode
4. **Verify compatibility**: Check that your inverter model is supported
5. **Review settings**: Carefully review all parameters before applying
6. **Test safely**: Implement settings during safe conditions with proper supervision

## 🔌 Setup Modes

Deye hybrid inverters support different physical configurations depending on your installation requirements:

- **Basic**: Standard solar + battery + backup loads (most common residential setup)
- **Generator**: Basic setup + backup generator for extended runtime
- **Smart-Load**: Basic setup + controllable non-essential loads for energy optimization
- **AC-Couple**: Basic setup + AC-coupled solar for system expansion
- **AC-Solar**: Battery system with AC-coupled solar only (retrofit applications)

See [Setup Modes Documentation](docs/setup-modes.md) for detailed connection diagrams and use cases.

## ⚡ Example Configuration

```text
configurations/europe/SUN-12K-SG04LP3-EU-Netherlands-Netbeheer-VDE4105-AC-Solar.md
├── Setup mode and connections
├── Grid requirements and standards
├── Specific inverter model details
├── Grid protection settings
├── Power quality parameters
├── Setup-specific AC-solar settings
├── Testing results
└── Installation notes
```

## 🛡️ Safety & Compliance

⚠️ **Important Safety Notes:**

- Always consult qualified electrical professionals before implementation
- Verify compliance with local grid codes and regulations  
- Test settings in safe conditions before final deployment
- Keep documentation of all applied settings
- Regular monitoring recommended after installation

## 📋 Configuration Format

Each configuration includes:

- **Setup Mode**: Physical connection configuration and requirements
- **Grid Requirements**: Voltage/frequency ranges, standards
- **Protection Settings**: Over/under voltage and frequency limits
- **Power Quality**: Power factor, reactive power control
- **Reconnection**: Timing and soft-start parameters
- **Setup-Specific Settings**: Generator control, load management, AC-coupling parameters
- **Testing Results**: Validation data and certification info
- **Installation Notes**: Special requirements and considerations

## 🤝 Contributing

We welcome contributions from:

- Solar installers and technicians
- Electrical engineers  
- Grid operators
- Certification bodies
- End users with verified settings

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines on:

- Submission process
- Documentation standards
- Testing requirements
- Quality guidelines

## 📖 Documentation

- [Setup Modes Guide](docs/setup-modes.md) - Physical configuration options and connection diagrams
- [Configuration Template](templates/configuration-template.md) - Standard format for new submissions
- [Inverter Models Reference](docs/inverter-models.md) - Complete model compatibility guide
- [Testing Guidelines](testing/README.md) - Validation and testing procedures

## 📄 License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## ⭐ Support the Project

- ⭐ Star this repository if you find it useful
- 🐛 Report issues or incorrect settings
- 🔧 Contribute new configurations for your region
- 📖 Improve documentation and guides
- 🌐 Help translate content to other languages

## 📞 Getting Help

- **Issues**: Use GitHub Issues for bug reports and questions
- **Discussions**: Join community discussions for general help
- **Documentation**: Check existing docs before asking questions

---

**Disclaimer**: This repository provides community-contributed settings for informational purposes. Always verify compliance with local regulations and consult qualified professionals. Contributors and maintainers assume no responsibility for damages or non-compliance resulting from use of these configurations.
