
# Weather Forecasting Project

This is a weather forecasting project built using Python, Django, and external APIs to predict the weather for a given location. The system provides real-time weather data such as temperature, humidity, wind speed, and weather conditions.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package manager)
- Django
- An API key from a weather service provider (e.g., OpenWeatherMap)

## Setup Instructions

### Step 1: Clone the Repository

Clone the repository to your local machine using the following command:

```bash
git clone https://github.com/Har2yQn78/weather-forecasting.git
cd weather-forecasting
```

### Step 2: Install Dependencies

Create a virtual environment and install all the required dependencies:

```bash
python -m venv venv
source venv/bin/activate  # For Linux/MacOS
venv\Scripts\activate     # For Windows
```

Then, install the required packages:

```bash
pip install -r requirements.txt
```

### Step 3: Configure the Weather API

1. Sign up for a weather API key at [OpenWeatherMap](https://openweathermap.org/api) or your chosen weather provider.
2. Store the API key in a `.env` file at the root of your project:

```
WEATHER_API_KEY=your_api_key_here
```

### Step 4: Set Up the Database

Run the following command to migrate the database and set up the necessary tables:

```bash
python manage.py migrate
```

### Step 5: Run the Development Server

To start the development server and test the application locally, run:

```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/` in your browser.

### Step 6: Accessing the Weather Data

Once the server is running, you can access the weather forecast for any location. The app provides an interface where you can enter the city name and get the weather data for that location.

## Features

- Displays current weather conditions (temperature, humidity, wind speed).
- Hourly and daily forecasts for up to 7 days.
- Search weather by city name.
- Beautiful, responsive UI using Django templates and CSS.

## Project Structure

```
weather_forecasting/
├── manage.py                # Django management script
├── weatherPredictionWebApp/  # Main project directory
│   ├── __init__.py
│   ├── settings.py           # Settings for the project
│   ├── urls.py               # URL routing configuration for the whole project
│   ├── wsgi.py               # WSGI application entry point
│   ├── asgi.py               # ASGI application entry point
│   ├── forecast/             # App for weather forecasting
│   │   ├── __init__.py
│   │   ├── admin.py          # Admin configuration
│   │   ├── apps.py           # App configuration
│   │   ├── models.py         # Data models
│   │   ├── views.py          # Views for handling requests
│   │   ├── urls.py           # URL routing configuration for the forecast app
│   │   ├── forms.py          # Forms for user input
│   │   ├── templates/        # Template files for views
│   │   │   └── weather.html  # Weather forecast page template
│   │   └── static/           # Static files (JS, CSS, images)
│   │       ├── js/           # JavaScript files
│   │       │   └── chartSetup.js
│   │       ├── css/          # CSS files
│   │       │   └── styles.css
│   │       └── img/          # Image files
│   │           └── (images)
└── .env                      # Environment variables (API keys, etc.)
```

## Technologies Used

- **Django**: The web framework used to build the application.
- **OpenWeatherMap API**: Provides weather data for different locations.
- **Python**: The primary programming language for the backend logic.
- **HTML/CSS**: For creating the frontend user interface.
- **JavaScript**: For enhancing the frontend experience with chart visualizations.
- **Chart.js** (via `chartSetup.js`): Used for charting weather data.

## Running Tests

If you have tests set up for your project, you can run them using:

```bash
python manage.py test
```

## Troubleshooting

- Ensure that your API key is correct and has the appropriate permissions to access weather data.
- If the server is not starting, check that all dependencies are installed correctly.

