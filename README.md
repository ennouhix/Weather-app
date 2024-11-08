# Weather App Controller - README

## Description

The `WeatherController` is a component of a simple weather application developed using Spring Boot. This controller retrieves and displays weather information for a specific city using the OpenWeatherMap API.

## Features

The controller handles two main actions:
1. **Home Page**: Displays the home page with a form to input a city name.
2. **Weather Display**: When a city is submitted through the form, it fetches weather data from the OpenWeatherMap API and displays:
   - The city and country names
   - The weather description
   - The temperature in Celsius
   - The humidity
   - The wind speed
   - An icon representing the weather condition

If an error occurs (e.g., city not found), the app redirects the user to an error page.

## Endpoints

### `/`

- **Method**: `GET`
- **Description**: Displays the home page with a form to input a city.
- **Returns**: The `index.html` view.

### `/weather`

- **Method**: `GET`
- **Parameters**:
  - `city`: The name of the city for which the weather information is requested.
- **Description**: Fetches weather data from the OpenWeatherMap API for the specified city.
- **Returns**: The `weather.html` view containing the weather data if the city is found. Otherwise, it redirects to the `error.html` view.

## Dependencies

- **Spring Boot**: Framework for building the application.
- **RestTemplate**: Used for making HTTP GET requests to the OpenWeatherMap API.
- **ModelAndView**: Used to pass data to the model and display the corresponding view.

## Configuration

The controller uses an API key that must be defined in the `application.properties` file:

```properties
api.key=YOUR_OPENWEATHERMAP_API_KEY
