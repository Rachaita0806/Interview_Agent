# Interview Trainer Agent

An AI-powered interview trainer using **IBM Granite 4 (ibm/granite-4-h-small)** via IBM Watson ML.

## 🚀 Quick Start

### 1. Install dependencies
```bash
npm install
```

### 2. Start the server
```bash
npm start
```
or for development with auto-reload:
```bash
npm run dev
```

### 3. Open the app
Visit [http://localhost:3000](http://localhost:3000)

---

## 📁 Project Structure
```
Interview_Agent/
├── server.js          ← Express backend + IBM Granite API integration
├── public/
│   └── index.html     ← Full frontend (chat UI)
├── package.json
└── README.md
```

## ⚙️ Configuration
The IBM credentials are pre-configured in `server.js`. To use a `.env` file instead, create one:
```
IBM_API_KEY=your_api_key
IBM_ML_URL=https://us-south.ml.cloud.ibm.com/ml/v1/text/generation?version=2023-05-29
MODEL_ID=ibm/granite-4-h-small
PROJECT_ID=b2f80dda-2ab7-410e-832f-53b41bee8a27
PORT=3000
```

## 🎯 Features
- Personalized mock interviews (Technical, HR, or Mixed)
- Difficulty adapts to your performance
- Scores answers out of 10 with detailed feedback
- Model answers provided
- Progress tracker across 10 questions
- Quick action buttons (hint, skip, repeat, progress check)
