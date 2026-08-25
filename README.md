Resume AI
Live Demo
https://furqanresumeanalyzer.netlify.app/
AI-powered resume analyzer that helps you improve your resume for ATS compatibility, content quality, skill coverage, and job matching.

Built with React, Vite, and Tailwind CSS, Resume AI provides AI-powered analysis and rewriting when an OpenAI API key is configured, while also supporting a deterministic local analyzer when no AI key is available.

Features

- 📄 Resume Upload — Upload and analyze your resume.
- 🤖 AI Resume Analysis — Get intelligent feedback on resume quality and content.
- 📊 ATS Score — Evaluate your resume for ATS compatibility.
- 🧠 Skill Coverage — Identify skills present in your resume and areas that may need improvement.
- 💼 Job Description Matching — Compare your resume against a job description.
- ✍️ AI Rewrite Suggestions — Improve resume content with AI-generated recommendations.
- 📑 PDF Export — Export your analyzed resume/report as a PDF.
- 🔄 JSON Export — Export analysis results as JSON.
- ⚡ Local Fallback Analyzer — Analyze resumes locally when an OpenAI API key is not configured.
- 🌐 Netlify Functions — Handle AI requests through server-side Netlify Functions.

How It Works

Resume AI supports two analysis modes.

AI Mode

When an "OPENAI_API_KEY" is configured, AI-powered features use OpenAI through a Netlify serverless function.

The OpenAI API key is kept on the server side and is not exposed to the browser.

Local Fallback Mode

When an OpenAI API key is not configured, Resume AI can use its deterministic local analyzer for core resume analysis.

This allows the application to provide useful resume analysis without requiring an external AI service.

Tech Stack

- React — Frontend UI
- Vite — Development server and build tool
- Tailwind CSS — Styling
- Netlify Functions — Server-side functionality
- OpenAI API — AI-powered analysis and rewriting
- JavaScript — Application logic

Requirements

Before running the project locally, make sure you have:

- Node.js
- npm
- Git

An OpenAI API key is optional if you want to use the local fallback analyzer.

Installation

Clone the repository:

git clone https://github.com/YOUR_USERNAME/resume-ai.git

Move into the project directory:

cd resume-ai

Install dependencies:

npm install

Run Locally

Start the development server:

npm run dev

Vite will provide a local URL, usually:

http://localhost:5173/

Open the URL in your browser.

Production Build

Create a production build with:

npm run build

To preview the production build locally:

npm run preview

OpenAI API Configuration

OpenAI integration is optional.

For AI-powered features, configure:

OPENAI_API_KEY=your_openai_api_key

The application expects the variable to be named exactly:

OPENAI_API_KEY

Do not use:

VITE_OPENAI_API_KEY

The API key should be configured server-side through Netlify environment variables.

Deploy to Netlify

Resume AI is configured for deployment on Netlify.

1. Push the Project to GitHub

Create a GitHub repository named:

resume-ai

Push the project files to the repository.

Do not commit:

- "node_modules/"
- ".env"
- OpenAI API keys

2. Import the Repository into Netlify

In Netlify, select:

Add new project → Import an existing project → GitHub

Select the "resume-ai" repository.

3. Build Settings

Use:

Build command: npm run build
Publish directory: dist

The existing "netlify.toml" handles the Netlify configuration and Functions setup.

4. Configure the OpenAI API Key

In your Netlify project, go to:

Project configuration → Environment variables

Add:

Key: OPENAI_API_KEY
Value: YOUR_OPENAI_API_KEY

Do not commit the API key to GitHub.

5. Deploy

Trigger a new deployment after configuring the environment variable.

Once deployment is complete, Netlify will provide a public URL for your application.

Security

The OpenAI API key should always remain server-side.

Never:

- Commit API keys to GitHub.
- Put API keys directly in React components.
- Expose API keys through frontend environment variables.
- Share API keys in screenshots or public repositories.

If an API key is accidentally exposed, revoke it and create a new one.

GitHub Repository Information

Repository name: "resume-ai"

Display name: "Resume AI"

Description:

«AI-powered resume analyzer that scores your resume for ATS compatibility, content quality, and skill coverage — with job-description matching, rewrite suggestions, and PDF/JSON export. Built with React, Vite, and Tailwind CSS.»

Suggested GitHub Topics

"react" "vite" "tailwindcss" "resume" "ats" "openai" "netlify" "job-search"

Development Workflow

A typical workflow is:

Edit code
   ↓
npm run dev
   ↓
Test locally
   ↓
git add .
   ↓
git commit
   ↓
git push
   ↓
Netlify deploys

Once GitHub and Netlify are connected, pushing changes to the configured branch can automatically trigger a new deployment.

License

This project is provided for educational and development purposes.

Add an appropriate open-source license if you intend to distribute the project publicly.
