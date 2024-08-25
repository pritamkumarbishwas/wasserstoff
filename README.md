
# Design a Weather Forecast Dashboard

This is a React-based weather forecast application that allows users to view the current weather and a 5-day forecast for any city. The app provides an option to toggle between Celsius and Fahrenheit for displaying temperature details.

## Features

- **Current Weather:** Displays current weather conditions for a specified city.
- **5-Day Forecast:** Provides a 5-day weather forecast with daily averages.
- **Temperature Unit Toggle:** Users can switch between Celsius and Fahrenheit.
- **Error Handling:** Displays appropriate error messages when an invalid city is entered or if there's an issue fetching the data.
- **Dynamic Weather Icons:** Displays weather icons based on the current weather conditions.

## How It Works

### 1. **State Management**
   - The app uses the `useState` and `useEffect` hooks for managing the application's state and side effects.
   - `search`: Tracks the city entered by the user.
   - `currentWeather`: Stores the current weather data fetched from the API.
   - `forecast`: Holds the 5-day forecast data.
   - `error`: Captures any error messages for user feedback.
   - `unit`: Tracks the unit of measurement (metric for Celsius or imperial for Fahrenheit).
   - `tempUnit`: Manages the display unit symbol (°C or °F).

### 2. **API Integration**
   - The app integrates with the [OpenWeatherMap API](https://openweathermap.org/api) to fetch weather data.
   - **API Endpoints Used:**
     - `https://api.openweathermap.org/data/2.5/weather`: For fetching current weather data.
     - `https://api.openweathermap.org/data/2.5/forecast`: For fetching 5-day forecast data.

### 3. **Fetching Weather Data**
   - The `fetchWeatherData` function fetches both the current weather and 5-day forecast data based on the user's search input.
   - It also handles errors, such as invalid city names or issues with the API, by setting an appropriate error message.

### 4. **Processing Forecast Data**
   - The `processForecast` function processes the raw forecast data to extract daily average temperatures and weather conditions.
   - The processed data is then stored in the `forecast` state and displayed to the user.

### 5. **Temperature Conversion**
   - The `convertTemperature` function converts temperatures between Celsius and Fahrenheit based on the selected unit.

### 6. **Dynamic Weather Icons**
   - The `getWeatherIcon` function returns the appropriate weather icon image based on the main weather condition (e.g., Clouds, Rain, Clear).

## Installation

### Prerequisites

- Node.js (v14 or higher)
- Git

### Steps

# Clone the repository
    git clone https://github.com/pritamkumarbishwas/wasserstoff
# Navigate to the project directory
   ```bash
      cd wasserstoff
      cd fullstackInternTask

# Install dependencies
   ```bash
   npm install

# Start the application
```bash
npm start
