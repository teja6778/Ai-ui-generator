# Ai-ui-generator
AI-powered UI generator using Next.js and Claude API
This an AI-powered web application that generates UI componets from user prompts using modern full-stack technologies.
---

##  Features

* Generate UI components using AI
* Chat-based interface
* Real-time code preview
* AI integration (Claude API)
* File system & editor support

---

## Tech Stack

* **Frontend:** Next.js, React, TypeScript
* **Backend:** API Routes (Next.js)
* **Database:** Prisma + SQLite
* **AI Integration:** Claude API
* **Styling:** Tailwind CSS

---

## Setup Instructions

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:3001
```

---

## Environment Variables

Create a `.env` file and add API key:

```env
ANTHROPIC_API_KEY=your_api_key_here
```

---

## Challenges & Fixes

### 1️. Hydration Error (Next.js)

**Problem:**
Server-rendered UI didn’t match client UI.

**Cause:**
Random IDs generated differently on server and client.

**Fix:**

* Disabled SSR for problematic components
* Used stable/static IDs

**What I learned:**
Understanding SSR vs CSR and hydration in React.

---

### 2️. Runtime Error (`trim()` issue)

**Problem:**

```
Cannot read properties of undefined (reading 'trim')
```

**Fix:**

```js
(input || "").trim()
```

**Learning:**
Handled undefined values safely in JavaScript.

---

### 3️. Module Not Found Error

**Problem:**
Missing dependency `@ai-sdk/react`

**Fix:**

```bash
npm install @ai-sdk/react ai
```

---

### 4️. CLI & Environment Issues

**Problem:**
Commands like `git` and `claude` not recognized.

**Fix:**

* Installed required tools
* Configured system PATH

---

## Key Learnings

* SSR vs CSR (Next.js)
* Debugging real-world frontend errors
* API integration with AI services
* Environment setup & CLI tools
* Writing production-ready code

---

## Future Improvements

* Authentication system
* Deploy on Vercel
* More UI templates
* Usage analytics

---

## Author
**Teja Peranathini**
