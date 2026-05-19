# 🌤 Weather App

A beautiful, real-time weather dashboard application that displays current weather conditions for any city in the world using the Open-Meteo API.

## Features

✨ **Key Features:**
- 🔍 **City Search** - Easily search for any city worldwide
- 🌡️ **Current Temperature** - Real-time temperature in Celsius
- 💨 **Wind Speed** - Current wind speed in km/h
- 🧭 **Wind Direction** - Wind direction in degrees
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- 🎨 **Modern UI** - Beautiful gradient background with glassmorphism effects
- ⚡ **Fast & Lightweight** - No external dependencies, pure HTML/CSS/JavaScript
- 🌐 **Free APIs** - Uses free, no-authentication-required APIs

## Demo

You can use the app directly by opening `index.html` in your web browser. The app will load immediately with no setup required!

## How It Works

1. **User enters a city name** in the search box
2. **Geocoding API** converts city name to coordinates (latitude/longitude)
3. **Weather API** fetches current weather data for those coordinates
4. **Results are displayed** with temperature, wind speed, and wind direction

### Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with gradients and backdrop filters
- **JavaScript (ES6+)** - Async/await for API calls
- **[Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api)** - Free city coordinate lookup
- **[Open-Meteo Weather API](https://open-meteo.com/en/docs)** - Free weather data

## Installation

### Option 1: Local File (Easiest)
1. Clone this repository:
   ```bash
   git clone https://github.com/solomon-hi/Weather-app.git
   cd Weather-app
   ```
2. Open `index.html` in your web browser
3. Start searching for cities!

### Option 2: Using a Local Server
For better security and performance with certain features:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using Live Server (VS Code extension)
# Just right-click index.html and select "Open with Live Server"
```

Then navigate to `http://localhost:8000` (or the port shown in your terminal)

## Usage

1. **Enter a city name** - Type any city name (e.g., "London", "New York", "Tokyo")
2. **Click the Search button** or press Enter
3. **View the weather** - Current temperature, wind speed, and direction are displayed
4. **Search again** - Enter another city to see its weather

### Example Queries

- "London" → London, United Kingdom
- "New York" → New York, United States  
- "Tokyo" → Tokyo, Japan
- "Paris" → Paris, France

## API Endpoints

### Geocoding (Get Coordinates)
```
GET https://geocoding-api.open-meteo.com/v1/search?name={city_name}
```
Returns the first matching city with latitude/longitude.

### Weather Data
```
GET https://api.open-meteo.com/v1/forecast?latitude={lat}&longitude={lon}&current_weather=true
```
Returns current weather including temperature, wind speed, and wind direction.

## Project Structure

```
Weather-app/
├── index.html          # Main application (HTML + CSS + JavaScript)
├── README.md          # This file - project documentation
├── CONTRIBUTING.md    # Contribution guidelines
└── LICENSE            # License information (optional)
```

## Browser Compatibility

✅ **Supported Browsers:**
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)

## Troubleshooting

### "City not found" Error
- Check the spelling of the city name
- Try with a larger city or country capital
- Some very small cities may not be in the geocoding database

### "Something went wrong" Error
- Check your internet connection
- The APIs might be temporarily down (rare)
- Check browser console (F12) for detailed error messages

### No results appear
- Ensure JavaScript is enabled in your browser
- Clear browser cache and reload
- Try opening in a different browser

## API Limits

Both APIs used are free and have generous rate limits:
- **Open-Meteo Geocoding API** - No authentication required, ~10 requests/second
- **Open-Meteo Weather API** - No authentication required, ~10 requests/second

For production use with higher demands, consider getting an API key.

## Future Enhancements

Potential features for future versions:
- [ ] 5-day weather forecast
- [ ] Historical weather data
- [ ] Weather alerts and notifications
- [ ] Multiple city comparison
- [ ] Weather condition icons (sunny, rainy, cloudy, etc.)
- [ ] Temperature unit toggle (Celsius/Fahrenheit)
- [ ] Local storage for favorite cities
- [ ] Geolocation-based weather (use user's current location)
- [ ] Dark/Light theme toggle
- [ ] Weather maps

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to:
- Report bugs
- Request features
- Submit pull requests
- Set up your development environment

## License

This project is open source and available under the MIT License.

## Credits

- Weather data provided by [Open-Meteo](https://open-meteo.com/) - Free weather API
- Geocoding data provided by [Open-Meteo](https://open-meteo.com/) - Free geocoding API

## Support

If you encounter any issues or have questions:
1. Check the [Troubleshooting](#troubleshooting) section above
2. Search existing [GitHub Issues](https://github.com/solomon-hi/Weather-app/issues)
3. Create a new GitHub Issue with a detailed description

---

Made with ❤️ by [Solomon](https://github.com/solomon-hi)
