````markdown
# Interview Trainer Agent

An AI-powered interview trainer using **IBM Granite 4 (`ibm/granite-4-h-small`)** via IBM Watson Machine Learning.

## 🚀 Quick Start

### 1. Install dependencies

```bash
npm install
````

### 2. Start the server

```bash
npm start
```

or for development with auto-reload:

```bash
npm run dev
```

### 3. Open the app

🚀 **Live Demo:** [https://interview-agent-ev2t.onrender.com](https://interview-agent-ev2t.onrender.com)

---

## 📁 Project Structure

```text
Interview_Agent/

├── server.js                         ← Express backend + IBM Granite API integration
├── public/
│   └── index.html                    ← Full frontend (chat UI)
├── Problem_Statements/
│   └── Interview_Trainer_Agent_Problem_Statement.pdf
├── Project_PPT/
│   └── Project presentation
├── Certificates/
│   └── Project certificates
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

> **Note:** The `.env` file is not included in GitHub because it contains sensitive API credentials.

## ⚙️ Configuration

The application uses environment variables for IBM credentials and configuration.

Create a `.env` file in the project root:

```env
IBM_API_KEY=your_api_key
IBM_ML_URL=https://us-south.ml.cloud.ibm.com/ml/v1/text/generation?version=2023-05-29
IBM_IAM_URL=https://iam.cloud.ibm.com/identity/token
MODEL_ID=ibm/granite-4-h-small
PROJECT_ID=your_project_id
PORT=3000
```

Never upload the `.env` file to GitHub.

## 🎯 Features

* Personalized mock interviews
* Technical, HR, and Mixed interview modes
* Difficulty adapts to candidate performance
* Scores answers out of 10
* Detailed feedback on candidate responses
* Identifies strengths and areas for improvement
* Provides model answers for comparison
* Generates the next interview question automatically
* Progress tracker across 10 questions
* Quick action buttons for hint, skip, repeat, and progress check
* Interactive question-and-answer interview flow
* Supports behavioral and entry-level Software Engineer interview preparation
* Structured AI evaluation for every response
* Maximum-question control to keep the interview focused
* Cloud deployment using Render

## 🔄 How It Works

1. The candidate opens the Interview Trainer Agent.
2. The candidate selects their interview preferences.
3. The agent generates an appropriate interview question.
4. The candidate submits their answer.
5. The answer is sent to the Node.js backend.
6. The backend securely communicates with IBM Watson Machine Learning.
7. IBM Granite evaluates the candidate's response.
8. The agent provides:

   * Score
   * What was good
   * What to improve
   * Model answer
   * Next question
9. The interview continues until the maximum number of questions is reached.

## 🧠 AI Evaluation Format

For every candidate response, the agent provides structured feedback:

```text
📊 Score: X/10

✅ What was good: ...

⚠️ What to improve: ...

💡 Model Answer: ...

❓ Next Question: ...
```

This helps candidates understand their performance and improve their interview responses.

## 🏗️ System Architecture

```text
Candidate
    │
    ▼
Interview Trainer Web Interface
    │
    ▼
Node.js + Express Backend
    │
    ▼
/api/chat
    │
    ▼
IBM Watson Machine Learning
    │
    ▼
IBM Granite 4 H Small
    │
    ▼
AI-generated Evaluation
    │
    ├── Score
    ├── Strengths
    ├── Improvement Tips
    └── Model Answer
    │
    ▼
Next Interview Question
    │
    ▼
Candidate
```

## 🛠️ Technologies Used

| Technology                  | Purpose                                        |
| --------------------------- | ---------------------------------------------- |
| IBM Granite 4 H Small       | AI-powered interview generation and evaluation |
| IBM Watson Machine Learning | Cloud-based AI model inference                 |
| IBM Cloud                   | AI and cloud infrastructure                    |
| Node.js                     | Backend runtime                                |
| Express.js                  | Backend server and API                         |
| HTML                        | Frontend structure                             |
| CSS                         | Frontend styling                               |
| JavaScript                  | Frontend interaction and API communication     |
| GitHub                      | Source code management                         |
| Render                      | Web application deployment                     |

## 🔐 Security

* IBM API credentials are stored using environment variables.
* The `.env` file is excluded from GitHub using `.gitignore`.
* API requests to IBM Watson Machine Learning are handled through the backend.
* IBM credentials are not exposed directly in the frontend.

## 🌐 Deployment

The application is deployed using Render.

🚀 **Live Demo:** [https://interview-agent-ev2t.onrender.com](https://interview-agent-ev2t.onrender.com)

The deployed application connects the frontend to the Node.js/Express backend, which communicates with IBM Watson Machine Learning and IBM Granite.

## 🎓 Project Objective

The objective of the Interview Trainer Agent is to provide students and fresh graduates with an interactive platform for practicing job interviews.

The agent simulates an interview environment and helps users improve their performance through realistic questions, structured evaluation, personalized feedback, model answers, and continuous practice.

## 📌 Project Highlights

* Uses **IBM Granite** as the AI model.
* Uses **IBM Watson Machine Learning** for model inference.
* Provides an interactive AI interview experience.
* Evaluates candidate responses automatically.
* Provides actionable feedback after each answer.
* Helps candidates practice both technical and soft skills.
* Provides a deployed web application accessible through the internet.

## 🔮 Future Scope

* Resume-based personalized interviews
* Job-description-based question generation
* RAG-based retrieval of role-specific interview resources
* Voice-based mock interviews
* Multilingual interview support
* Interview performance analytics
* Technical coding interview mode
* Industry-specific interview preparation
* Company-specific interview preparation
* Integration with additional AI agents

## 📂 Project Resources

* **GitHub Repository:** [https://github.com/Rachaita0806/Interview_Agent](https://github.com/Rachaita0806/Interview_Agent)
* **Live Demo:** [https://interview-agent-ev2t.onrender.com](https://interview-agent-ev2t.onrender.com)
* **Problem Statement:** `Problem_Statements/Interview_Agent.pdf`
* **Project Presentation:** `Project_PPT/`
* **Certificates:** `Certificates/`

## 👩‍💻 Author

**Rachaita Bhattacharjee**

B.Tech Computer Science Engineering (Data Science)

KIIT Deemed to be University

```

### One thing I intentionally changed

I moved **RAG** to **Future Scope** rather than claiming it is already implemented. Your official problem statement describes the Interview Trainer Agent as RAG-powered, but your current application uses Granite directly without a retrieval component. So this README remains accurate while still showing that RAG is part of the intended future development.
```
