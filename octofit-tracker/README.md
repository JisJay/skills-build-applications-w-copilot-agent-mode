# OctoFit Tracker - Multi-Tier Application

A modern multi-tier application for activity tracking with user authentication, team management, and competitive leaderboards.

## Project Architecture

### Technology Stack

**Frontend (Presentation Tier)**
- React 19 with Vite
- React Router DOM for navigation
- Bootstrap for styling
- Port: 5173

**Backend (Logic Tier)**
- Node.js with Express
- TypeScript for type safety
- CORS middleware for cross-origin requests
- Port: 8000

**Data Tier**
- MongoDB for data persistence
- Mongoose for schema management and data access
- Port: 27017

## Project Structure

```
octofit-tracker/
├── frontend/          # React + Vite application
│   ├── src/
│   ├── package.json
│   └── vite.config.js
└── backend/           # Express + TypeScript application
    ├── src/
    ├── dist/          # Compiled JavaScript
    ├── package.json
    └── tsconfig.json
```

## Getting Started

### Prerequisites

- Node.js (LTS version)
- MongoDB (running locally or connection URI available)
- npm or yarn

### Installation

#### Backend Setup

```bash
cd octofit-tracker/backend
cp .env.example .env
npm install
```

Update `.env` with your configuration if needed.

#### Frontend Setup

```bash
cd octofit-tracker/frontend
npm install
```

### Running the Application

#### Start MongoDB

```bash
# Check if MongoDB is running
ps aux | grep mongod

# If not running, start MongoDB service
# The application expects MongoDB on mongodb://localhost:27017
```

#### Start Backend Development Server

```bash
cd octofit-tracker/backend
npm run dev
```

The backend API will be available at `http://localhost:8000`

Health check endpoint: `http://localhost:8000/api/health`

#### Start Frontend Development Server

```bash
cd octofit-tracker/frontend
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Building for Production

#### Backend

```bash
cd octofit-tracker/backend
npm run build
npm start
```

#### Frontend

```bash
cd octofit-tracker/frontend
npm run build
npm run preview
```

## Development

### Backend Development Scripts

- `npm run dev` - Run development server with ts-node
- `npm run build` - Compile TypeScript to JavaScript
- `npm run start` - Run compiled production build

### Frontend Development Scripts

- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Environment Variables

### Backend (.env)

```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
NODE_ENV=development
```

## API Endpoints

### Health Check
- `GET /api/health` - Check API status

## Features (Planned)

- User authentication and profiles
- Activity logging and tracking
- Team creation and management
- Competitive leaderboard
- Personalized workout suggestions

## License

ISC
