# JanSathi — Har Nagrik Ka Digital Saathi

**PromptWars x Global Prompt Challenge Submission**
Vertical: Smart Bharat – AI-Powered Civic Companion

## 🔗 Links
- **Live Demo:** https://smart-bharat-ai-civic-companion-750416859101.asia-southeast1.run.app/
- **GitHub Repo:** https://github.com/anandraj1999/jansathi

## 📌 Problem Statement
Citizens in India often struggle to navigate government services — understanding scheme eligibility, knowing which documents are required, or reporting civic issues through the right channel. Information is scattered, jargon-heavy, and rarely available in a citizen's preferred language.

**JanSathi** solves this with a single GenAI-powered civic companion — every citizen's digital saathi — that simplifies government information, helps citizens report issues, recommends relevant schemes, and guides document requirements, in the language they speak.

## ✨ Features
- **AI Chat Assistant** – conversational interface answering civic and government service queries in plain language
- **Smart Complaint Reporter** – structured complaint filing with categorization, tracked under a dedicated Complaints tab
- **Scheme Recommender** – suggests relevant government schemes with eligibility context
- **Document Checklist Assistant** – returns required documents and guidance for common government processes
- **Bilingual Support** – full English and Hindi language support
- **Voice Input** – voice-based interaction for accessibility and ease of use
- **FAQ Tab** – quick answers to common citizen questions
- **Validation Suite** – built-in scenario testing to verify core flows work correctly
- **Authenticated Experience** – dedicated auth/login screen for personalized sessions
- **Custom UI/Animation** – 3D welcome avatar and animated tricolor wave for a distinctive, on-brand civic-tech feel

## 🧠 AI / Prompt Workflow & Strategy
JanSathi is powered by the **Google Gemini API** via the `@google/genai` SDK, with an Express server layer handling API calls securely (keeping the Gemini API key server-side, never exposed to the client).

The assistant logic is built around **intent-based routing**:
1. **Intent detection** – incoming user messages are classified into flows: general query, complaint, scheme lookup, or document help
2. **Structured extraction** – for complaints, the model extracts category, description, and urgency into a structured `ComplaintData` object rendered via a dedicated `ComplaintCard` component
3. **Contextual recommendations** – for scheme queries, the model reasons over user-provided context to recommend relevant schemes via `SchemeCard`
4. **Bilingual response generation** – responses are generated in the user's selected language using a centralized `translations` layer for UI text and language-aware prompting for AI-generated content
5. **Built-in validation** – the `ValidationSuite` component runs sample scenarios against the live AI flows to confirm functional correctness before submission

This architecture keeps the AI logic centralized and testable, while the UI stays modular and easy to extend with new civic-service flows.

## 🛠️ Tech Stack
- **Frontend:** React 19 + TypeScript, Vite, Tailwind CSS, Framer Motion (`motion`)
- **Backend:** Express (Node.js/TypeScript) as the API layer
- **AI:** Google Gemini API (`@google/genai`)
- **Icons:** Lucide React
- **Deployment:** Google Cloud Run (asia-southeast1)
- **Built with:** Google AI Studio


## 👤 Team
ANAND RAJ
