# Klimate Weather App

A modern, responsive weather application built with React, TypeScript, and Vite. It provides current weather, 5-day forecasts, and more, using OpenWeatherMap API data.

## Features

- 🌤️ View current weather conditions for any city
- 📅 5-day weather forecast with temperature, humidity, wind, and more
- 📍 Geolocation support to get weather for your current location
- ⭐ Mark favourite cities for quick access
- 🌓 Light/Dark theme toggle
- 🔍 Search cities with autocomplete
- ⚡ Fast, responsive UI with skeleton loading states

## Tech Stack

- **React 19** + **TypeScript**
- **Vite** for blazing fast development
- **Tailwind CSS** for styling
- **@tanstack/react-query** for data fetching and caching
- **Radix UI** and **Lucide Icons** for accessible UI components
- **OpenWeatherMap API** for weather data

## Getting Started

### Prerequisites
- Node.js (v18 or newer recommended)
- npm or yarn

### Installation

```bash
git clone https://github.com/your-username/weatherapp.git
cd weatherapp
npm install
```

### Running the App

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
```

### Linting

```bash
npm run lint
```

## Project Structure

```
src/
  api/           # API config and types
  assets/        # Images and icons
  components/    # Reusable UI and weather components
  context/       # Theme and global context providers
  hooks/         # Custom React hooks
  lib/           # Utility functions
  pages/         # Main pages (Dashboard, CityPage)
  App.tsx        # Main app component
  main.tsx       # Entry point
public/          # Static assets
```

## Environment Variables

Create a `.env` file in the root with your OpenWeatherMap API key:

```
VITE_OPENWEATHER_API_KEY=your_api_key_here
```

## Credits
- Weather data from [OpenWeatherMap](https://openweathermap.org/)
- UI inspired by modern weather dashboards

## License

MIT
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
