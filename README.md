# Insightly 
# AI POWERED ASTROLOGY AND NUMEROLOGY Platform
## Complete Technical Documentation

## Table of Contents
1. [Deployment](#deployment)
2. [Project Overview](#project-overview)
3. [System Architecture](#system-architecture)
4. [Frontend Implementation](#frontend-implementation)
5. [Backend Implementation](#backend-implementation)
6. [LangFlow Integration](#langflow-integration)
7. [Technical Specifications](#technical-specifications)
8. [API Documentation](#api-documentation)
9. [Data Structure](#data-structure)

## Deployment

### Live Application
- Production URL: [https://supermind-728e46.webflow.io/](https://supermind-728e46.webflow.io/)
- Platform: Render
- Status: Active

### Deployment Infrastructure
- Frontend: Render Web Services
- Database: DataStax Astra DB
- AI Integration: Langflow & Gemini

## Project Overview

### Objective
To provide personalized astrology and numerology insights based on user-provided details such as name, date of birth, time, and location. The platform offers daily, monthly, and life predictions powered by Gemini AI.

### Core Components
- Gemini AI for astrology-based chatbot interaction
- Astra DB for horoscope data storage and retrieval
- React-based frontend
- Node.js proxy backend
- Gemini integration

### Key Features
- Horoscope Generation: Daily, monthly, and yearly predictions
- Personalized Recommendations: Gemstones, rituals, and meditation practices
- AI-Powered Chatbot: Gemini-driven conversational spiritual guidance
- Astrological Insights: Career, relationships, health, and more
- Interactive Dashboard: View and manage horoscope details


## System Architecture

### Frontend Layer
1. **Landing Page**
   - Description based on working of model
   - Input based form
   - Canvas which shows information of Astrological and Numerological prediction.
   - Header with navigation
   - Features-> AI chatbot which show prediction
   - Team information
   - Call-to-action elements

2. **Analytics Dashboard**
   - Personalized horoscope cards
   - Monthly gemstone and flower recommendations
   - Daily meditation suggestions

### Backend Layer
1. **Proxy Server**
   - Handles communication between frontend and Gemini AI
   - Error management 
   - Response optimization

2. **Data Processing**
   - Text splitting and chunking
   - Data parsing
   - Parsing of astrological data from Astra DB
   - Integration with LangFlow for horoscope workflows


## Frontend Implementation

### Dashboard Components

#### Performance Overview Cards
```typescript
interface HoroscopeMetrics {
  flower: string;
  gemstone: string;
  prediction: string;
}
```

### State Management
```typescript
interface DashboardState {
  posts: PostData[];
  dateRange: [Date, Date];
  selectedPostTypes: string[];
  sortBy: string;
  sortOrder: 'asc' | 'desc';
  currentPage: number;
  filters: {
    search: string;
    minEngagement?: number;
    maxEngagement?: number;
  };
}
```

## Backend Implementation

### Server Setup
```javascript
const express = require('express');
const http = require('http');
const WebSocket = require('ws');
const cors = require('cors');

const app = express();
const server = http.createServer(app);
const wss = new WebSocket.Server({ server });
```

### WebSocket Management
- Unique requestId assignment
- Connection tracking
- Real-time data streaming
- Error handling

### API Endpoints
1. **Chat Endpoint**
   - Handles client requests
   - Forwards to Langflow API
   - Streams responses
   - Error management

## LangFlow Integration

### Pipeline Components

1. **File Input**
   - Loads JSON data containing monthly horoscope insights.
   - Path: monthly_horoscope_data.json

2. **Text Processing**
   - Chunk size: 500
   - Overlap: 200
   - Custom separators :-Based on months, zodiac signs, or themes (e.g., career, relationships).

3. **Astra DB Integration**
   - Database: `soulbuddy_db`
   - Collection: `horoscopes`
   - Embedding Model: Astra Vectorize
   - Provider: OGemini
   - Model: `Gemini AI`

4. **Gemini Integration**
   - Model: `gemini-1.5-pro`
   - Temperature: 0.1
   - Streaming enabled:- Real-time response generation for interactive chatbot experiences.

## Technical Specifications

### Design Guidelines
1. **Color Palette**
   - Primary: #4B0082
   - Secondary: #9370DB
   - Accent: #FFD700
   - Background: #F3F4F6
   - Text: #1A202C


2. **Typography**
   - Headings: Playfair Display
   - Body: Open Sans
   - Monospace: Source Code Pro

3. **Responsive Design**
   - Mobile: 320px - 480px
   - Tablet: 481px - 768px
   - Desktop: 769px+

### Performance Optimizations
1. **Frontend**
   - Lazy loading of horoscope data.
   - Caching user preferences for faster predictions.
   - Optimized assets for quick rendering of charts and cards.

2. **Backend**
   - Efficient database queries using Astra DB.
   - Response batching for frequent horoscope queries.
   - Real-time streaming of Gemini responses.

### Testing Strategy
1. **Unit Testing**
   - Horoscope parsing and formatting tests.
   - Validation of user-input fields (e.g., date, time).

2. **Integration Testing**
   - API endpoint testing for horoscope generation.
   - Gemini model testing for response accuracy.

3. **End-to-End Testing**
   - User flow testing: From input to personalized predictions.
   - Performance testing for real-time response rendering.

## API Documentation

### Endpoints

1. **Chat API**
```javascript
POST /chat
{
  "input_value": string,
  "birth_details": {
    "name": string,
    "date": string,
    "time": string,
    "city": string
  }
}

```

2. **Analytics API**
```javascript
GET /api/horoscope
Query Parameters:
- month: string (e.g., "January")
- sign: string (e.g., "Leo")
- detailLevel: string ("daily", "monthly", "yearly")
- recommendations: boolean (Include gemstone and flower insights)

```

## Data Structure

### Horoscope Data Model
```typescript
interface HoroscopeData {
  month: string;
  zodiac_sign: string;
  flower: string;
  gemstone: string;
  prediction: {
    career: string;
    relationships: string;
    health: string;
  };
}

```

### User Detailed Model
```typescript
interface UserDetails {
  name: string;
  birth_date: string;
  birth_time: string;
  city: string;
  zodiac_sign: string;
}

```

This documentation reflects the SoulBuddy platform's focus on astrology and numerology while integrating Gemini AI. 
#   c o n q u e r o r 
 
 
