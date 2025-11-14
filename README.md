# Cloudlytic - Cloud Cost Optimization Dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow.svg)](https://powerbi.microsoft.com/)

A comprehensive Power BI dashboard for comparing and optimizing cloud infrastructure costs between Microsoft Azure and AWS.

![Cloudlytic Dashboard](https://via.placeholder.com/800x400?text=Cloudlytic+Dashboard+Preview)

## Features

- **Multi-Cloud Cost Comparison**: Side-by-side comparison of Azure and AWS pricing
- **Service Categories**: Compute, Storage, and Network cost analysis
- **Cost Optimization**: Automated identification of cost-saving opportunities
- **Forecasting**: Monthly expense predictions based on usage trends
- **Automated Data Refresh**: Integration with Excel and cloud BOMs
- **Interactive Visualizations**: Drill-down capabilities and dynamic filtering

## Demo

Try it out with sample data - no cloud credentials required! Just run the sample data generator and open the dashboard.

## Project Structure

```
Cloudlytic/
├── data/                          # Data sources and staging
│   ├── azure_pricing.xlsx         # Azure pricing data
│   ├── aws_pricing.xlsx           # AWS pricing data
│   ├── cloud_bom.xlsx             # Bill of Materials
│   └── usage_trends.xlsx          # Historical usage data
├── scripts/                       # Data collection and processing
│   ├── azure_pricing_collector.py # Azure pricing API integration
│   ├── aws_pricing_collector.py   # AWS pricing API integration
│   ├── data_processor.py          # Data transformation and cleaning
│   └── cost_optimizer.py          # Cost optimization logic
├── powerbi/                       # Power BI files
│   └── Cloudlytic_Dashboard.pbix  # Main dashboard file
├── config/                        # Configuration files
│   └── config.json                # API keys and settings
└── docs/                          # Documentation
    ├── setup_guide.md             # Setup instructions
    └── user_guide.md              # User manual
```

## Quick Start

### Option 1: Using Sample Data (Recommended for Testing)

```bash
# Clone the repository
git clone https://github.com/yourusername/cloudlytic.git
cd cloudlytic

# Install dependencies
pip install -r requirements.txt

# Generate sample data
python scripts/create_sample_data.py

# Build the Power BI dashboard following the guide
# See powerbi/Dashboard_Build_Guide.md
```

### Option 2: Using Live Cloud Data

```bash
# Install dependencies
pip install -r requirements.txt

# Configure your credentials
cp config/config.example.json config/config.json
# Edit config/config.json with your Azure/AWS credentials

# Collect live pricing data
python scripts/azure_pricing_collector.py
python scripts/aws_pricing_collector.py

# Process and optimize
python scripts/data_processor.py
python scripts/cost_optimizer.py

# Build the Power BI dashboard
# See powerbi/Dashboard_Build_Guide.md
```

## Requirements

- Python 3.8+
- Power BI Desktop
- Azure/AWS API access (optional for live data)
- Excel 2016+ (for data staging)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/cloudlytic.git
cd cloudlytic
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Set up configuration:
```bash
cp config/config.example.json config/config.json
```

4. (Optional) Add your cloud credentials to `config/config.json`

## Usage

### Generate Sample Data

Perfect for testing and demonstrations:

```bash
python scripts/create_sample_data.py
```

This creates realistic sample data for:
- Azure pricing (30 services)
- AWS pricing (30 services)
- 12 months of usage trends
- Bill of Materials with 10 resources

### Collect Live Data

If you have cloud credentials configured:

```bash
# Collect Azure pricing
python scripts/azure_pricing_collector.py

# Collect AWS pricing
python scripts/aws_pricing_collector.py

# Process the collected data
python scripts/data_processor.py

# Generate optimization insights
python scripts/cost_optimizer.py
```

### Build the Dashboard

Follow the comprehensive guide in `powerbi/Dashboard_Build_Guide.md` to create your Power BI dashboard with:
- Executive Summary
- Cost Comparison
- Usage Trends
- Cost Optimization
- Cost Forecast
- Bill of Materials

## Documentation

- [Setup Guide](docs/setup_guide.md) - Detailed installation and configuration
- [User Guide](docs/user_guide.md) - How to use the dashboard
- [Dashboard Build Guide](powerbi/Dashboard_Build_Guide.md) - Step-by-step Power BI instructions
- [DAX Measures](powerbi/DAX_Measures.txt) - All Power BI measures and calculations

## Project Structure

```
Cloudlytic/
├── data/                          # Data files (gitignored)
├── scripts/                       # Python data collection scripts
│   ├── azure_pricing_collector.py
│   ├── aws_pricing_collector.py
│   ├── data_processor.py
│   ├── cost_optimizer.py
│   └── create_sample_data.py
├── powerbi/                       # Power BI resources
│   ├── Dashboard_Build_Guide.md
│   └── DAX_Measures.txt
├── config/                        # Configuration files
│   └── config.example.json
├── docs/                          # Documentation
│   ├── setup_guide.md
│   └── user_guide.md
├── requirements.txt               # Python dependencies
└── README.md
```

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Azure Retail Prices API
- AWS Price List API
- Power BI Community

## Support

For issues, questions, or contributions:
- Open an issue on GitHub
- Check the documentation in `docs/`
- Review the setup guide for troubleshooting

## Roadmap

- [ ] Add GCP pricing support
- [ ] Implement automated testing
- [ ] Create Docker container for easy deployment
- [ ] Add CI/CD pipeline
- [ ] Develop web-based dashboard alternative
- [ ] Add more optimization algorithms

## Screenshots

Coming soon - build the dashboard and add your own!

---

Made with ❤️ for cloud cost optimization
