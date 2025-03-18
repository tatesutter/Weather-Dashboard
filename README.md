# Weather API Service

## Overview
This project is a weather API service that allows users to retrieve weather information for a specified city and store their search history. The application is built using Node.js with Express.js, and it integrates with the OpenWeatherMap API to fetch real-time weather data. The search history is stored locally.

## Features
- Retrieve current weather information for a specified city.
- Save search history to track previously searched cities.
- Fetch search history.
- Delete a city from search history.
- Serve a client-side application from the `dist` folder.

## Technologies Used
- Node.js
- Express.js
- TypeScript (optional but included in the type definitions)
- OpenWeatherMap API
- dotenv (for environment variables)
- File system (`fs/promises`) for storing search history

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/weather-api-service.git
   cd weather-api-service
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:
   ```env
   PORT=3001
   WEATHER_API_KEY=your_openweathermap_api_key
   ```

4. Start the server:
   ```sh
   npm start
   ```

## API Endpoints

### `POST /api/weather`
**Description:** Fetches weather data for a given city and saves it to search history.
**Request Body:**
```json
{
  "city": "New York"
}
```
**Response:**
```json
{
  "temperature": 22,
  "description": "clear sky",
  "city": "New York"
}
```

### `GET /api/history`
**Description:** Retrieves the list of previously searched cities.
**Response:**
```json
[
  { "id": "17123456789", "name": "New York" },
  { "id": "17198765432", "name": "Los Angeles" }
]
```

### `DELETE /api/history/:id`
**Description:** Removes a city from the search history.
**Response:**
```json
{
  "message": "City removed from search history"
}
```


## Contributing
If you'd like to contribute, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License.

## Contact
For any questions, reach out at [https://github.com/tatesutter].

