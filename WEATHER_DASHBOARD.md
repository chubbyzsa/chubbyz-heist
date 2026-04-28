# Weather Dashboard

A modern, responsive weather dashboard that fetches real-time weather data from the **OpenWeatherMap API**. Built with vanilla HTML, CSS, and JavaScript - no dependencies required!

## Features

✨ **Real-Time Weather Data**
- Current weather conditions with temperature, humidity, pressure, and more
- Wind speed and visibility information
- Cloud coverage percentage
- "Feels like" temperature

📊 **5-Day Forecast**
- Extended weather forecast
- Daily weather conditions and temperatures

🎨 **Beautiful UI**
- Modern gradient background
- Responsive card-based layout
- Weather emoji indicators
- Smooth animations and hover effects
- Mobile-friendly design

🔍 **Easy Search**
- Search any city worldwide
- Preset city buttons (London, New York, Tokyo, Paris, Sydney)
- Instant search results

## How to Use

1. **Open the Dashboard**
   - Open `weather-dashboard.html` in your web browser

2. **Search for a City**
   - Type a city name in the search box
   - Press Enter or click the Search button
   - Or click one of the preset city buttons

3. **View Weather Information**
   - Current weather with emoji indicators
   - Detailed metrics (humidity, wind speed, pressure, etc.)
   - 5-day forecast

## API Information

This dashboard uses the **OpenWeatherMap API** (free tier):

- **API Endpoint**: `https://api.openweathermap.org/data/2.5`
- **Features Used**:
  - `geo/1.0/direct` - Geocoding (convert city name to coordinates)
  - `weather` - Current weather data
  - `forecast` - 5-day weather forecast

- **Rate Limit**: 60 API calls/minute (free tier)
- **Data Units**: Metric (Celsius, m/s)

## Technical Details

### Technologies
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **API**: OpenWeatherMap REST API
- **No Dependencies**: Pure JavaScript, no frameworks or libraries

### Key Features in Code
- Async/Await for API calls
- Error handling and user feedback
- Loading states
- Responsive grid layout
- Weather emoji mapping
- Mobile-responsive design

### Weather Emoji Mapping
The dashboard maps weather descriptions to relevant emojis:
- ☀️ Clear sky
- 🌤️ Few clouds
- ☁️ Scattered/Broken clouds
- 🌧️ Rain/Shower
- ⛈️ Thunderstorm
- ❄️ Snow
- 🌫️ Fog/Mist
- And more!

## API Response Example

```json
{
  "coord": {"lon": -0.1276, "lat": 51.5085},
  "weather": [{"id": 803, "main": "Clouds", "description": "broken clouds"}],
  "main": {
    "temp": 15.2,
    "feels_like": 14.8,
    "temp_min": 12.5,
    "temp_max": 17.1,
    "pressure": 1013,
    "humidity": 72
  },
  "wind": {"speed": 4.5, "deg": 230},
  "clouds": {"all": 75},
  "visibility": 10000,
  "dt": 1699564800
}
```

## Customization

### Change Temperature Units
In the fetch URLs, change `units=metric` to `units=imperial` for Fahrenheit

### Add More Cities
Edit the preset buttons in the HTML:
```html
<button class="preset-btn" onclick="searchWeatherByCity('Your City')">Your City</button>
```

### Modify Styling
Edit the CSS variables in the `<style>` section to customize colors, fonts, and spacing

## Browser Compatibility

- Chrome/Chromium
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile)

## Limitations

- **Free Tier**: Limited to 60 API calls per minute
- **No Historical Data**: Only current and forecast data
- **No Paid Features**: Advanced data not available on free tier

## Future Enhancements

- [ ] Local storage for favorite cities
- [ ] Weather alerts
- [ ] Historical weather data
- [ ] Air quality index
- [ ] UV index
- [ ] Pollen forecast
- [ ] Dark/Light theme toggle
- [ ] Hourly forecast

## License

Open source - feel free to use and modify!

## Attribution

Weather data provided by [OpenWeatherMap](https://openweathermap.org/)

---

**Made with ❤️ by CHUBBYZ**
