# AI Resume Analyzer

AI Resume Analyzer is a SaaS web application that analyzes resumes and provides an **ATS compatibility score along with AI-generated feedback** to help users improve their resumes for job applications.

The system allows users to upload resumes, evaluates them based on common ATS standards, and generates suggestions using AI to improve keywords, structure, and overall resume quality.

---

## Tech Stack

**Frontend**
- React
- Vite
- Tailwind CSS
- React Router
- Axios

**Backend**
- Node.js
- Express.js

**Database**
- PostgreSQL

**AI Integration**
- OpenAI API (gpt-4o-mini)

---

## Key Features

- Resume upload and analysis  
- AI-generated feedback and improvement suggestions  
- ATS compatibility score generation  
- Secure user authentication using JWT  
- Fast and responsive UI with React and Tailwind  
- Resume history storage for users  

---

## Running the Project

### 1. Start Backend

```bash
cd backend
cp .env.example .env
npm install
npm run dev
```

Update `.env` file with:

```
DATABASE_URL=
JWT_SECRET=
OPENAI_API_KEY=
```

---

### 2. Start Frontend

```bash
cd frontend
npm install
npm run dev
```

---

### 3. Setup Database

Create a PostgreSQL database and set `DATABASE_URL`:

```
postgresql://username:password@localhost:5432/ai_resume_analyzer
```

Database tables are created automatically when the backend starts.

---

## API Base URL

The frontend proxies `/api` requests to:

```
http://localhost:5000
```

So the backend must run on **port 5000** for the frontend to work correctly.

---

## Project Structure

```
backend/
 ├── controllers
 ├── routes
 ├── middleware
 ├── services
 ├── db
 └── server.js

frontend/
 └── src
     ├── components
     ├── pages
     ├── services
     └── context
```

---

## Future Improvements

- Resume keyword optimization suggestions  
- Support for multiple resume formats  
- Analytics dashboard for resume performance  
- Resume comparison feature  
