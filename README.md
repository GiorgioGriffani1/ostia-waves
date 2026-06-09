# 🌊 OSTIA WAVES

Community platform for organizing surf, beach volley, and social activities at Ostia, Rome.

## Features

- 🗺️ Interactive map with real-time wave data
- 🌊 Live surf conditions (wind, swell, wave height)
- 📅 Event listings from Resident Advisor
- 👥 Community sessions (surf, beach volley)
- 🏐 Court booking system
- 💬 In-app messaging
- 🎥 Live webcams

## Tech Stack

- **Frontend**: Vanilla JavaScript, Leaflet (maps), Chart.js
- **Backend**: Supabase (PostgreSQL, Auth, RLS)
- **Hosting**: Cloudflare Pages
- **Data**: Open-Meteo, Surfline, Windguru, RA Events

## Setup

### Prerequisites
- Node.js 18+
- GitHub account
- Supabase account
- Cloudflare account

### Installation

```bash
# Clone repo
git clone https://github.com/YOUR_USERNAME/ostia-waves.git
cd ostia-waves

# Install dependencies
npm install

# Local dev
npm run dev

# Deploy to Cloudflare Pages
npm run deploy
```

## Environment Variables

Create `.env.local`:

```
VITE_SUPABASE_URL=https://myqhzmimrbtsagcktrhz.supabase.co
VITE_SUPABASE_KEY=sb_publishable_CPEVLQ28fVz2hYNOII6M1A_LLTo0xPb
```

## Supabase Schema

Tables:
- `profiles` - User profiles
- `sessions` - Surf/beach/volley sessions
- `session_participants` - Who's joining sessions
- `courts` - Beach volley courts
- `court_slots` - Time slots for courts
- `messages` - In-session chat

All tables have RLS (Row Level Security) enabled.

## Deployment

Push to GitHub → Cloudflare Pages auto-deploys on every commit.

## License

MIT
