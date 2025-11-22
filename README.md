# Multi-Agent Tourism System

A complete React-based multi-agent tourism system that provides weather information and tourist attraction recommendations for any location.

## Features

- **Parent AI Agent**: Smart heuristic-based analysis (works without API keys!) with optional Claude API enhancement
- **Weather Agent**: Fetches current temperature and precipitation probability using Open-Meteo API
- **Places Agent**: Finds tourist attractions using Overpass API and Nominatim
- **Error Handling**: Validates locations and provides user-friendly error messages
- **Modern UI**: Clean, responsive design with Tailwind CSS
- **100% Free**: Works completely without any paid API keys

## Setup

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

3. (Optional) Enter your Claude API key in the app for enhanced AI analysis, or use it completely free without any API keys!

## API Keys

- **Claude API Key**: Optional - The system works completely free without it! Enhanced AI analysis available if you have a key from [Anthropic Console](https://console.anthropic.com/)
- **Open-Meteo API**: No key required (free)
- **Nominatim API**: No key required (free, but requires User-Agent header)
- **Overpass API**: No key required (free)

**🎉 The system is 100% FREE to use!** It uses smart heuristics for intent detection and location extraction. Claude API is only an optional enhancement.

## Usage Examples

1. **Places only**: "I'm going to go to Bangalore, let's plan my trip."
2. **Weather only**: "I'm going to go to Bangalore, what is the temperature there?"
3. **Both**: "I'm going to go to Bangalore, what is the temperature there? And what are the places I can visit?"
4. **Invalid location**: "Tell me about Xyz12345" → Returns error message

## Project Structure

```
├── src/
│   ├── agents/
│   │   ├── parentAgent.js      # Main orchestrator agent
│   │   ├── weatherAgent.js      # Weather data agent
│   │   └── placesAgent.js       # Tourist places agent
│   ├── utils/
│   │   └── api.js               # API utility functions
│   ├── App.jsx                  # Main React component
│   ├── main.jsx                 # React entry point
│   └── index.css               # Tailwind CSS imports
├── package.json
├── vite.config.js
├── tailwind.config.js
└── postcss.config.js
```

## Technologies

- React 18
- Vite
- Tailwind CSS
- Claude API (Anthropic)
- Open-Meteo API
- Nominatim API
- Overpass API

## Error Handling

The system handles:
- Invalid/non-existent locations
- API failures
- Network errors
- Missing API keys

All errors are displayed in a user-friendly format.

