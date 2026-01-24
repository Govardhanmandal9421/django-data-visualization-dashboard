# Data Visualization Dashboard

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Django](https://img.shields.io/badge/django-6.0.1-green)
![License](https://img.shields.io/badge/license-MIT-blue)

A Django web application for generating and displaying data visualizations with interactive charts and paginated data tables.

## Features

- 📊 Multiple chart types: Bar, Scatter, Histogram, Box, Violin, and Line plots
- 📋 Paginated data table with 10 records per page
- 🎨 Modern responsive UI with smooth animations
- 📱 Mobile-friendly design
- 🔧 Automatic data generation using Faker
- 🖼️ Chart image generation and storage

## Technologies Used

- **Backend**: Django 6.0.1
- **Database**: SQLite3
- **Data Generation**: Faker
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Frontend**: HTML, CSS, JavaScript

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Data_V
```

2. Create a virtual environment:
```bash
python -m venv venv
```

3. Activate the virtual environment:
```bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

5. Run database migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

6. Start the development server:
```bash
python manage.py runserver
```

7. Open your browser and navigate to `http://127.0.0.1:8000/`

## Usage

The application automatically generates sample data and creates various charts when you visit the dashboard. The main features include:

- **Charts Section**: Displays 6 different types of visualizations
- **Data Table**: Shows paginated user data with search and navigation
- **Responsive Design**: Works on desktop and mobile devices

## Project Structure

```
Data_V/
├── Data_V/                 # Main Django project settings
├── Data_vi/               # Main application
│   ├── migrations/        # Database migrations
│   ├── models.py         # Data models
│   ├── views.py          # View functions
│   └── demo.py           # Data generation and chart creation
├── Templates/             # HTML templates
├── public/                # Static and media files
├── manage.py             # Django management script
└── requirements.txt      # Python dependencies
```

## Models

### Data Model
- `name`: Character field
- `age`: Integer field
- `gender`: Character field
- `city`: Character field
- `state`: Character field
- `country`: Character field
- `email`: Email field

### Chart Model
- Stores paths to generated chart images for each chart type

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

[Your Name]

## Acknowledgments

- Django documentation
- Faker library for data generation
- Matplotlib and Seaborn for visualization