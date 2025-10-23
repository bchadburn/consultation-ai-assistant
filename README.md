# Healthcare Consultation Assistant (Demonstration application only)

An AI-powered SaaS application that  generate healthcare related summaries, action items, and patient-friendly emails from consultation notes.

## Features

- 📋 **Professional Summaries**: Generate comprehensive medical record summaries
- ✅ **Action Items**: Clear next steps and follow-up actions
- 📧 **Patient Emails**: Draft patient-friendly communications
- 🔐 **Secure Authentication**: Clerk-based user management
- 💳 **Subscription Management**: Premium plan protection
- 🎨 **Modern UI**: Responsive design with dark mode support

## Tech Stack

### Frontend
- **Next.js 15** with TypeScript
- **Tailwind CSS** for styling
- **React Hooks** for state management
- **Server-Sent Events** for real-time streaming
- **React Markdown** for content rendering

### Backend
- **FastAPI** with Python 3.11+
- **Pydantic** for data validation
- **OpenAI API** for AI generation
- **JWT Authentication** with Clerk

### Development
- **Hybrid Architecture** - Node.js frontend + Python backend
- **Vercel Deployment**


## Project Structure
saas/
├── api/
│ └── index.py # FastAPI backend
├── pages/
│ ├── app.tsx # App configuration
│ ├── index.tsx # Landing page
│ └── product.tsx # Consultation form
├── styles/
│ └── globals.css # Global styles
├── package.json # Node.js dependencies
├── pyproject.toml # Python dependencies
└── README.md


## Getting Started

### Prerequisites
- Node.js 18+
- Python 3.11+
- OpenAI API key
- Clerk account

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd saas
   ```

2. **Install Node.js dependencies**
   ```bash
   npm install
   ```

3. **Install Python dependencies**
   ```bash
   uv sync
   ```

4. **Set up environment variables**
   ```bash
   # Create .env.local
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_key
   CLERK_SECRET_KEY=your_clerk_secret
   CLERK_JWKS_URL=your_jwks_url
   OPENAI_API_KEY=your_openai_key
   ```

5. **Run the development server**
   ```bash
   # Terminal 1: Next.js frontend
   npm run dev
   
   # Terminal 2: FastAPI backend
   uvicorn api.index:app --reload --port 8000
   ```

## Usage

1. **Sign up/Sign in** using Clerk authentication
2. **Subscribe** to the premium plan
3. **Fill out the consultation form** with:
   - Patient name
   - Visit date
   - Detailed consultation notes
4. **Generate AI-powered content** including:
   - Professional summary for medical records
   - Next steps for the doctor
   - Patient-friendly email draft

## License

MIT License - see LICENSE file for details
