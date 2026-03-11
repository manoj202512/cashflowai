# CashFlowAI

> AI-powered invoice-to-cash platform that autonomously recovers unpaid invoices using AI agents.

## Architecture Overview

```
cashflowai/
├── backend/          # FastAPI backend
├── frontend/         # Next.js 14 dashboard
├── workers/          # n8n automation workflows
├── ai/               # LangChain AI agents
├── infra/            # Docker & deployment configs
└── scripts/          # Utility scripts
```

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js 14 + Tailwind CSS |
| Backend | FastAPI (Python) |
| Database | Supabase PostgreSQL |
| Auth | Supabase Auth |
| AI Orchestration | LangChain |
| Voice AI | ElevenLabs API |
| Email | Resend API |
| Payments | Stripe API |
| Automation | n8n |
| Deployment | Vercel + Railway |

## Quick Start

### Prerequisites
- Node.js 18+
- Python 3.11+
- Docker & Docker Compose
- Supabase project

### 1. Clone & Configure
```bash
git clone https://github.com/manoj202512/cashflowai
cd cashflowai
cp .env.example .env
# Fill in your API keys in .env
```

### 2. Start with Docker
```bash
docker-compose up --build
```

### 3. Manual Dev Setup
```bash
# Backend
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload

# Frontend
cd frontend
npm install
npm run dev
```

## Features

- **Multi-tenant SaaS** with per-tenant quotas
- **Invoice Sync** from QuickBooks & Xero
- **AI Risk Scoring** (0-100) per invoice
- **Autonomous Collections** via email, SMS, voice calls
- **AI Voice Agent** powered by ElevenLabs
- **Smart Follow-Up Engine** with channel & timing optimization
- **Invoice Blocker Detection** (missing PO, wrong contact, etc.)
- **Cash Flow Forecasting** (7/30/90 day)
- **Legal Escalation** with demand letter generation
- **Stripe Billing** with subscription management

## Business Model

- Implementation Fee: $10,000 one-time
- Monthly Subscription: $1,500–$2,500/month

## Deployment

- Frontend: Vercel
- Backend: Railway
- Database: Supabase
- Workers: Railway or self-hosted

## Environment Variables

See `.env.example` for all required environment variables.

## License

MIT
