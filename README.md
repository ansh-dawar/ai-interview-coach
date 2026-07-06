# AI Interview Coach

AI Interview Coach is an AI-powered mock interview platform that helps users prepare for interviews by analyzing their resume, generating personalized interview questions, and evaluating their answers with AI feedback.

The platform uses a **FastAPI backend**, **React + Vite frontend**, and **Groq LLaMA 3.1** for AI-powered question generation and answer evaluation.

---

## Live Demo

Frontend: https://ai-interview-coach-ecdh.vercel.app

---

## Features

* Upload PDF resume
* Extract and analyze resume content
* Classify candidate level as fresher, intermediate, or expert
* Generate personalized interview questions
* Regenerate questions to avoid repetition
* Submit answers for AI evaluation
* Get score, strengths, and weaknesses
* Responsive and modern user interface
* Light/Dark theme support

---

## Tech Stack

### Frontend

* React 18
* Vite
* Tailwind CSS
* React Router DOM
* Axios

### Backend

* FastAPI
* Python
* Groq API
* LLaMA 3.1 8B Instant
* PyPDF2
* Uvicorn
* Python Dotenv

---

## Project Structure

```txt
ai-interview-coach/
│
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
│
└── ai-interview-coach/
    ├── index.html
    ├── package.json
    ├── vite.config.js
    ├── tailwind.config.js
    ├── postcss.config.js
    ├── .env.example
    │
    └── src/
        ├── components/
        ├── hooks/
        ├── layouts/
        ├── pages/
        ├── routes/
        ├── services/
        ├── utils/
        ├── App.jsx
        ├── main.jsx
        └── index.css
```

---

## API Endpoints

| Method | Endpoint               | Description                                 |
| ------ | ---------------------- | ------------------------------------------- |
| GET    | `/`                    | Checks if the backend API is running        |
| POST   | `/upload_resume`       | Uploads and extracts text from a PDF resume |
| GET    | `/ask_question`        | Generates a personalized interview question |
| GET    | `/regenerate_question` | Generates a different interview question    |
| POST   | `/evaluate`            | Evaluates the submitted answer              |

---

## Getting Started

### Prerequisites

Make sure you have installed:

* Python 3.8+
* Node.js 18+
* npm
* Groq API Key

---

## Backend Setup

Clone the repository:

```bash
git clone https://github.com/ansh-dawar/ai-interview-coach.git
cd ai-interview-coach
```

Install backend dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file in the root folder:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Run the backend server:

```bash
uvicorn main:app --reload
```

Backend will run on:

```txt
http://localhost:8000
```

---

## Frontend Setup

Go to the frontend folder:

```bash
cd ai-interview-coach
```

Install frontend dependencies:

```bash
npm install
```

Create a `.env` file inside the frontend folder:

```env
VITE_API_URL=http://localhost:8000
```

Run the frontend:

```bash
npm run dev
```

Frontend will run on:

```txt
http://localhost:5173
```

---

## Environment Variables

### Backend `.env`

```env
GROQ_API_KEY=your_groq_api_key_here
```

### Frontend `.env`

```env
VITE_API_URL=http://localhost:8000
```

---

## How It Works

1. User uploads a PDF resume.
2. Backend extracts text from the resume using PyPDF2.
3. Groq LLaMA analyzes the resume and identifies the candidate level.
4. AI generates interview questions based on resume content and experience level.
5. User submits an answer.
6. AI evaluates the answer and returns feedback with score, strengths, and weaknesses.

---

## Deployment

### Frontend Deployment

The frontend can be deployed on Vercel.

Recommended settings:

```txt
Framework: Vite
Root Directory: ai-interview-coach
Build Command: npm run build
Output Directory: dist
```

Add this environment variable in Vercel:

```env
VITE_API_URL=your_backend_url
```

### Backend Deployment

The backend can be deployed on Render.

Recommended settings:

```txt
Build Command: pip install -r requirements.txt
Start Command: uvicorn main:app --host 0.0.0.0 --port 8000
```

Add this environment variable in Render:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

## Important Notes

* Do not upload your `.env` file to GitHub.
* Keep your Groq API key private.
* Upload only PDF resumes.
* The backend currently stores resume text temporarily during runtime.

---

## Future Improvements

* User authentication
* Interview session history
* Multiple interview categories
* Voice-based interview answers
* Resume improvement suggestions
* Database integration
* Better analytics dashboard

---

## Author

**Shivansh Dawar**

GitHub: https://github.com/ansh-dawar

---

