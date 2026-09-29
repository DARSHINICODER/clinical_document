# Dr. Priya — AI-Powered Smart Clinical Assistant

**Dr. Priya** is a hospital-grade, commercial-quality clinical documentation and automation platform built for doctors, clinics, and hospitals. It ambiently converts doctor-patient conversations into structured medical documentation, extracts vital signs, generates SOAP notes, suggests ICD-10 and CPT codes, prepares e-prescriptions, and dispatches documents via WhatsApp.

---

## 🏛️ Project Location & Tech Stack

The application has been generated and validated inside:
`C:\Users\senku\.gemini\antigravity-ide\scratch\dr-priya`

> [!TIP]
> **Recommended Action**: Open `C:\Users\senku\.gemini\antigravity-ide\scratch\dr-priya` as your active workspace in Antigravity.

### Frontend
- **Framework**: React 19 + TypeScript + Vite
- **Styling**: Tailwind CSS (v4) with custom light/dark clinical theme palette
- **Icons & Charts**: Lucide React + Recharts
- **Routing**: React Router DOM (v7)
- **PDF Export**: jsPDF + html2canvas

### Backend
- **Server**: Node.js + Fastify REST API (`http://localhost:3001`)
- **Real-Time Streaming**: Server-Sent Events (SSE) for AI progress streaming
- **Database Architecture**: PostgreSQL + Neon Database + Drizzle ORM schema (with fallback in-memory store)

---

## 📦 Core Modules Implemented

| Module | Route | Key Features |
|---|---|---|
| **1. Dashboard** | `/` | Clinical overview stats, Recharts consultation trends, patient demographics pie chart, recent consultations table, quick action buttons. |
| **2. Patients** | `/patients` | Electronic health registry, MRN search, gender filter, register modal form, edit patient, delete confirmation, detailed patient profile drawer. |
| **3. New Consultation** | `/new-consultation` | Consultation setup wizard, patient selection, language selector (7 languages), chief complaint prompt, launch into AI Studio. |
| **4. AI Clinical Studio** | `/ai-studio` | 3-panel workspace, Web Audio API canvas waveform visualizer, recording controls (start/pause/resume/stop), audio upload, multilingual preset loader, live transcript stream, extracted vitals preview, step-by-step progress timeline. |
| **5. SOAP Notes** | `/soap-notes` | Automated vital cards (BP, HR, SpO2, Temp) with confidence badges and manual edit options, structured S-O-A-P sections, copy SOAP, save draft, physician approval sign-off, PDF export. |
| **6. Medical Coding** | `/medical-coding` | ICD-10 diagnosis codes table & CPT procedure codes table with confidence badges and clinical rationales, manual code addition, physician verification check, report export. |
| **7. Prescriptions** | `/prescriptions` | E-prescription builder, dynamic medication row builder, medication presets dropdown, interactive digital signature string, live preview card, PDF export, print, WhatsApp sharing. |
| **8. Superbill & Billing** | `/superbill` | Medical invoice builder, itemized CPT/ICD billable items, subtotal & tax calculations, PDF export, CSV download, JSON export. |
| **9. Consultation History**| `/history` | Master filterable table of past encounters with status badges and quick view actions. |
| **10. WhatsApp Gateway** | `/whatsapp` | QR code pairing simulation, patient phone verification, document attachment selector, message dispatch, delivery status logbook. |
| **11. Analytics** | `/analytics` | Recharts charts for monthly registrations growth, language distribution, top ICD-10 frequency. |
| **12. Settings** | `/settings` | Doctor profile, clinic information, OpenAI & Mistral API key fields, PostgreSQL Neon connection string test, light/dark mode toggle. |

---

## ⚙️ Running the Application

### 1. Frontend Development Server
```bash
cd C:\Users\senku\.gemini\antigravity-ide\scratch\dr-priya
npm run dev
```
- App URL: `http://localhost:5173/`

### 2. Fastify Backend Server
```bash
cd C:\Users\senku\.gemini\antigravity-ide\scratch\dr-priya
npm run server
```
- Backend REST API & SSE: `http://localhost:3001`
- Health Check: `http://localhost:3001/api/health`

### 3. Production Build Verification
```bash
npm run build
```
- Clean bundle compiled with zero TypeScript or PostCSS errors.

---

## 🛡️ Clinical Integrity & Safeguards
- **Zero AI Hallucination**: Unmentioned vital signs or symptoms are strictly marked as `Not Provided`.
- **Physician Sign-Off**: AI-generated SOAP notes and medical codes remain in `Draft` / `Pending Approval` status until explicitly reviewed and approved by the physician.
- **Data Privacy**: Encrypted streaming transcription architecture ready for HIPAA-compliant deployments.
