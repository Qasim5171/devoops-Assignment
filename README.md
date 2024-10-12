
**Weather App**

## **Project Overview**

The **Weather App** is a Flask-based web application that allows users to retrieve real-time weather data for any city, state, or country around the world. The app fetches data from the OpenWeatherMap API, including the current temperature, weather condition (e.g., clouds, rain, etc.), and an associated weather icon. Additionally, the app dynamically updates the background based on the weather condition, providing a visually engaging experience similar to modern mobile weather apps.

The app is designed to be minimalistic, responsive, and user-friendly, focusing on delivering essential weather information with a sleek design inspired by iPhone weather apps.

## **Features**

- **Real-time Weather Data**: Users can input the city, state, and country to get the latest weather updates, including:
  - Main weather condition (e.g., Clouds, Rain, Clear).
  - Detailed weather description (e.g., "overcast clouds").
  - Temperature (converted from Kelvin to Celsius).
  - Dynamic weather icons from OpenWeatherMap.

- **Dynamic Background**: The background changes based on the weather condition (e.g., sunny, cloudy, rainy), enhancing user experience.

- **Responsive Design**: The app is mobile-friendly and adjusts to different screen sizes. It's built using Bootstrap and custom CSS to ensure a consistent layout on both desktop and mobile devices.

- **Clean, Modern UI**: The app incorporates a frosted glass effect, a gradient background, and smooth fonts for a modern look.

## **Technology Stack**

- **Back-End**: Python with Flask framework.
- **Front-End**: HTML5, CSS3 (with Bootstrap for layout), JavaScript for dynamic elements.
- **API**: OpenWeatherMap API to fetch weather data.
- **Styling**: Google Fonts (Roboto), custom CSS for styling elements.

## **Project Structure**

```
/weather-app-project
    /static                # Static files (CSS, JS, images)
        sunny.jpg
        cloudy.jpg
        rainy.jpg
        snow.jpg
    /templates             # HTML templates
        index.html
    app.py                 # Main Flask application
    requirements.txt       # Python dependencies
    README.md              # Project documentation
```

## **How It Works**

1. **User Input**: 
   - The user enters the city, state, and country they want to get weather information for.
   
2. **API Call**: 
   - The app makes a GET request to the OpenWeatherMap API with the user's input.
   - The API returns the current weather data, including temperature, weather condition, and an icon representing the weather.

3. **Data Processing**: 
   - The server processes the weather data and passes it to the front-end to display.
   - The temperature is converted from Kelvin to Celsius before being shown.

4. **Dynamic Display**: 
   - The weather condition and temperature are displayed on the front-end along with a weather icon.
   - The background dynamically changes based on the weather condition (e.g., sunny background for clear weather, rainy background for rain).

5. **Responsive Design**: 
   - The app adjusts its layout for different screen sizes, ensuring a user-friendly experience on mobile devices.

## **Dependencies**

The app uses the following Python packages, which are listed in the `requirements.txt` file:

- **Flask**: A lightweight WSGI web application framework.
- **Requests**: For making HTTP requests to the OpenWeatherMap API.
- **python-dotenv**: To load environment variables (optional, if using `.env` for API keys).

To install the required dependencies, run:
```bash
pip install -r requirements.txt
```

## **Installation & Setup Instructions**

### **Prerequisites**

Ensure you have the following installed on your machine:

- **Python 3.8+**
- **PIP (Python Package Installer)**

### **Step-by-Step Installation**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/weather-app.git
   cd weather-app
   ```

2. **Install Dependencies**:
   Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up OpenWeatherMap API Key**:
   - Go to [OpenWeatherMap](https://home.openweathermap.org/users/sign_up) and sign up for an API key.
   - Replace `'your_openweathermap_api_key'` in the `app.py` file with your actual API key.

4. **Run the Flask Application**:
   Run the Flask app locally using:
   ```bash
   python app.py
   ```

5. **Access the Application**:
   Open your browser and go to `http://127.0.0.1:5000/`.

## **API Reference**

The app utilizes the OpenWeatherMap API to fetch real-time weather data. Below is the structure of the API call:

```python
url = f'https://api.openweathermap.org/data/2.5/weather?q={city},{state},{country}&appid={api_key}'
```

- **`q`**: Query parameter for city, state, and country (comma-separated).
- **`appid`**: Your API key from OpenWeatherMap.

Example Response:
```json
{
  "weather": [
    {
      "main": "Clouds",
      "description": "overcast clouds",
      "icon": "04d"
    }
  ],
  "main": {
    "temp": 289.92
  }
}
```

## **Potential Enhancements**

- **Hourly Forecast**: Extend the app to display hourly weather updates.
- **Unit Toggle**: Add an option for users to toggle between Celsius and Fahrenheit.
- **Geolocation**: Automatically detect the user’s location and show weather data based on their current coordinates.
- **Additional Weather Data**: Include humidity, wind speed, and UV index.

## **Contributors**

-  Muhammad Qasim(221026)
- Esham Afzal (221008)
- Aisha Munir(221004)

---

![image](https://github.com/user-attachments/assets/caf8740d-faea-4c11-aa1b-5916c8281cd1)

![image](https://github.com/user-attachments/assets/e6e3f337-58a4-475d-a27a-42ebabe062d0)

![image](https://github.com/user-attachments/assets/6b88d9db-2e01-4aed-8850-d6264e627682)





