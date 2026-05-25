<div align="center">
  <br />
  <h1>PYTHAFLOW.</h1>
  <p><strong>A Premium Digital Creative Agency built with Next.js, Three.js, and AI</strong></p>
  <br />
</div>

## ✦ Overview

**Pythaflow** is a state-of-the-art, full-stack landing page and management dashboard designed for a modern creative agency. It combines stunning 3D visual experiences with a robust, zero-cost backend infrastructure.

From interactive hero elements powered by `react-three-fiber` to a fully automated AI brand audit engine via OpenRouter, this repository represents the pinnacle of modern web design and backend efficiency.

## 🚀 Key Features

### 🎨 Premium Frontend Experience
*   **Next.js 14 App Router:** Blazing fast React rendering and seamless routing.
*   **Dynamic Theming:** Smooth transitions between Light and Dark modes with unified CSS variables.
*   **Three.js / R3F Integration:** An interactive, responsive `CircleNet` 3D background that responds to user mouse movements.
*   **Immersive Micro-Animations:** Custom keyframe animations, glassmorphism, and responsive grid layouts.

### 🧠 Free AI Brand Auditor
*   **OpenRouter Integration:** Connects seamlessly to `meta-llama/llama-3-8b-instruct:free` to parse user links and industry data.
*   **Automated JSON Reports:** Returns a structured brand audit scoring Website, SEO, Social, Content, Ads, and Strategy.
*   **Lead Capture:** Persists all generated audit requests to the database to schedule follow-up strategy calls.

### ⚙️ Zero-Cost Backend Infrastructure
*   **Prisma + SQLite:** A fully functional local database (`dev.db`) requiring zero third-party hosting fees.
*   **Automated Email Routing:** Utilizes `nodemailer` and Gmail SMTP to instantly notify administrators when a new project inquiry is submitted.
*   **Secure Admin Dashboard:** A protected `/admin` route powered by `jose` (JWT). Review all inquiries and audit requests through a clean, internal interface.

---

## 🛠️ Tech Stack

*   **Framework:** [Next.js](https://nextjs.org/) (App Router)
*   **Styling:** Vanilla CSS + CSS Modules
*   **3D Graphics:** [Three.js](https://threejs.org/) & [@react-three/fiber](https://docs.pmnd.rs/react-three-fiber/)
*   **Database:** [Prisma](https://www.prisma.io/) ORM with SQLite
*   **Authentication:** JWT via [jose](https://github.com/panva/jose)
*   **Email Processing:** [Nodemailer](https://nodemailer.com/)

---

## 💻 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/pythaflow.git
cd pythaflow
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Variables
Create a `.env.local` file in the root of the project:
```env
# Database connection for Prisma
DATABASE_URL="file:./dev.db"

# Admin Dashboard Password (Default: admin123)
ADMIN_PASSWORD="your-secure-password"

# JWT Secret for Admin Panel Cookies
JWT_SECRET="generate-a-random-secure-string"

# Gmail App Password for contact form emails
GMAIL_APP_PASSWORD="your-google-app-password"

# OpenRouter API Key for the Free Brand Audit
OPENROUTER_API_KEY="your-openrouter-key"
```

### 4. Initialize Database
```bash
npx prisma db push
```

### 5. Start Development Server
```bash
npm run dev
```
Navigate to `http://localhost:3000` to view the site, and `http://localhost:3000/admin` to access the dashboard.

---

## 📂 Project Structure

```text
├── app/
│   ├── admin/           # Secured JWT Admin Dashboard
│   ├── api/             # Backend API Routes (Assess, Contact, Auth)
│   ├── assessment/      # Free AI Brand Audit Form & Results
│   ├── contact/         # Project Inquiry Form
│   ├── services/        # Service Offerings Page
│   └── page.js          # Main Landing Page with 3D Hero Slider
├── components/          # Reusable UI (Navbar, Footer, Cursor, CircleNet)
├── lib/                 # Core Utilities (Prisma Client, Rate Limiting)
├── prisma/              # Database Schema (schema.prisma)
└── public/              # Static Assets (Slider Images, Favicon)
```

<div align="center">
  <br/>
  <i>Built with passion by the Pythaflow Team.</i>
</div>
