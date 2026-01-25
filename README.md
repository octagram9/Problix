# 🚀 Problix  
### Turning real-world problems into clear product ideas


## ✨ What is Problix?

**Problix** is a product-thinking tool that helps you go from a **raw problem statement** to a **clear, structured MVP plan**.

Instead of guessing:
- What should I build?
- Which features actually matter?
- Is this idea even worth pursuing?

Problix gives you **clarity before execution**.

You describe a problem in plain English — Problix turns it into something you can realistically build.


## 🧠 What Problix Does

From a single problem input, Problix generates:

- 🔍 **Problem Analysis**  
  Understands the real pain point and its context

- 💡 **Product Idea & Positioning**  
  Defines what to build, for whom, and why it matters

- 🧩 **Feature Breakdown**  
  Separates core features from advanced and AI-driven ones

- 🛠 **Tech Stack Suggestions**  
  Practical recommendations for frontend, backend, and tools

- 🗺 **MVP Roadmap**  
  A phased plan to move from idea → working product

All outputs are structured, readable, and immediately actionable.

## 🎯 Who is this for?

Problix is useful for:
- Founders validating an idea
- Developers planning side projects
- Product thinkers structuring MVPs
- Teams stuck at the “idea chaos” stage

If you’ve ever had a good idea but didn’t know **where to start**, Problix is built for you.


## 🏗 How it Works

- A clean **Next.js frontend** collects the problem input
- A **FastAPI backend** handles orchestration and logic
- Modular AI pipelines generate each output step
- A prompt-driven design keeps the system transparent and flexible

Problix can run using **mock intelligence** for safe testing or switch to **real AI** when configured.


## 🧰 Tech Stack

**Frontend**
- Next.js 14 (App Router)
- Tailwind CSS

**Backend**
- FastAPI (Python)
- Pydantic

**AI**
- Google Gemini via `google-genai`
- Prompt-based generation


## 📁 Project Structure

```text
backend/
├── main.py                     # FastAPI app & routes
├── ai/
│   ├── problem_parser.py       # Problem analysis
│   ├── idea_generator.py       # Product ideation
│   ├── feature_generator.py    # Feature breakdown
│   ├── tech_stack_generator.py # Tech stack suggestions
│   ├── mvp_roadmap_generator.py# MVP roadmap
│   └── prompts/               # Prompt templates
└── schemas/                    # Pydantic models

frontend/
├── app/                        # Next.js App Router
├── components/                 # UI components
└── lib/                        # API helpers & config
```
## ⚡ Getting Started

### Prerequisites
- Python 3.10+
- Node.js 18+
- pnpm / npm / yarn

### ▶ Backend Setup
```
python -m venv .venv
.venv\Scripts\activate
pip install -r backend/requirements.txt
```

Create `backend/.env`:

AI_MODE=mock
```
# GOOGLE_API_KEY=your_key_here
# GEMINI_MODEL=gemini-2.5-flash
# PROMPT_DIR=C:\absolute\path\to\custom_prompts
```

Run backend:
```
uvicorn backend.main:app --reload --port 8000
```
API Docs:
```
http://127.0.0.1:8000/docs
```


### ▶ Frontend Setup
```
cd frontend
pnpm install   # or npm install / yarn
```

Create `frontend/.env.local`:
```
NEXT_PUBLIC_API_BASE=http://127.0.0.1:8000
```
Run frontend:
```
pnpm dev
```


## 🔌 API Endpoints

POST endpoints:
- /analyze-problem
- /generate-idea
- /generate-features
- /generate-tech-stack
- /generate-mvp-roadmap
Example request:
```
{
  "problem": "Your problem statement here"
}
```

## 🧠 Prompt System

Prompt templates live in:

backend/ai/prompts/
To customize behavior:
1. Copy prompts to another folder
2. Set PROMPT_DIR in backend/.env
3. Problix will load them automatically


## 🔐 Security & Safety

- API keys are never committed
- .env files are gitignored
- Mock mode is enabled by default
- Live AI requires explicit configuration

Problix exists to make the early stage of building products **clearer, calmer, and more intentional**.
