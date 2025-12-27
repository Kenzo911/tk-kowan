# 🌍 WanderLust AI

An AI-powered travel itinerary generator that creates personalized trip plans with cost estimates.

![WanderLust AI](https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=800&auto=format&fit=crop)

## ✨ Features

- **AI-Powered Itineraries**: Leverages GPT-4o to generate detailed day-by-day travel plans
- **Cost Estimates**: Get realistic budget breakdowns for flights, accommodation, food, and activities
- **Beautiful UI**: Modern glassmorphism design with smooth animations
- **Customizable**: Adjust destination, duration, budget level, and personal interests

## 🛠️ Tech Stack

### Backend
- Node.js + Express
- OpenAI SDK (GPT-4o)
- CORS + dotenv

### Frontend
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- Framer Motion
- Lucide React Icons
- Axios

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ installed
- OpenAI API key

### 1. Setup Backend

```bash
cd backend

# Add your OpenAI API key to .env
# Edit .env and replace 'your_openai_api_key_here' with your actual key

# Start the server
node server.js
```

The backend will run on `http://localhost:5000`

### 2. Setup Frontend

```bash
cd frontend

# Start the development server
npm run dev
```

The frontend will run on `http://localhost:3000`

## 📁 Project Structure

```
ai_travel_buddy/
├── backend/
│   ├── server.js          # Express API server
│   ├── .env               # Environment variables (add your API key here)
│   └── package.json
├── frontend/
│   ├── src/
│   │   └── app/
│   │       ├── page.tsx       # Main application page
│   │       ├── globals.css    # Global styles
│   │       └── layout.tsx     # Root layout
│   ├── package.json
│   └── tailwind.config.ts
└── README.md
```

## 🔑 Environment Variables

### Backend (.env)
```
OPENAI_API_KEY=your_openai_api_key_here
PORT=5000
```

## 🎨 UI Preview

The application features:
- Dark theme with a stunning Earth/map background
- Glassmorphism input card with translucent styling
- Animated cost breakdown cards
- Alternating timeline layout for the itinerary
- Smooth Framer Motion animations throughout

## 📝 API Endpoint

### POST /api/itinerary

**Request Body:**
```json
{
  "destination": "Tokyo, Japan",
  "days": 7,
  "budget": "Moderate",
  "interests": "food, culture, anime"
}
```

**Response:**
```json
{
  "success": true,
  "destination": "Tokyo, Japan",
  "days": 7,
  "budget": "Moderate",
  "itinerary": {
    "summary": "...",
    "currency": "JPY",
    "costs": {
      "flights": "$800-$1200",
      "accommodation": "$700-$1000",
      "food": "$50-$80/day",
      "activities": "$200-$350",
      "total": "$2000-$3000"
    },
    "schedule": [...]
  }
}
```

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

MIT License - feel free to use this project for your own purposes.

---

Made with ❤️ by WanderLust AI
