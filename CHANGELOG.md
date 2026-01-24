# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-01-24

### Added
- Initial release of Data Visualization Dashboard
- Django web application with data visualization features
- Multiple chart types: Bar, Scatter, Histogram, Box, Violin, and Line plots
- Paginated data table with 10 records per page
- Automatic data generation using Faker library
- Responsive web design with modern UI
- Docker support with docker-compose configuration
- Comprehensive documentation including:
  - README with installation guide
  - Deployment guide for various platforms
  - Contribution guidelines
  - Environment variable configuration
- Automated setup scripts for Windows and Linux/macOS
- Proper .gitignore configuration
- MIT License

### Features
- **Data Management**: CRUD operations for user data
- **Chart Generation**: Automatic generation of 6 different chart types
- **Pagination**: Efficient data pagination for better performance
- **Responsive Design**: Mobile-friendly interface
- **Security**: Environment-based configuration for production deployment

### Dependencies
- Django 6.0.1
- Faker 35.0.0
- NumPy 2.2.2
- Pandas 3.1.0
- Matplotlib 3.10.0
- Seaborn 0.14.0
- Plotly 6.10.0
- Pillow 12.0.0

### Technical Details
- SQLite database for development
- PostgreSQL support for production
- Static file management
- Media file handling for chart images
- Custom management commands ready for extension