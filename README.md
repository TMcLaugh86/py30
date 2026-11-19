# 🐍 Py30 — 30 Days of Python

A mobile-first, interactive Python learning web application modeled after the *30 Days of Python* curriculum. Built as a zero-backend single-page application, **Py30** executes real Python 3.12 code directly inside the browser using WebAssembly and includes **PyBuddy**, a context-aware Python tutor.

🔗 **Live App:**
                 https://30daysofpython.netlify.app/
---

## ✨ Key Features

- **Real In-Browser Python 3.12 Runtime:** Powered by [Pyodide](https://pyodide.org/) (WebAssembly), running real Python code with live `stdout`/`stderr` console output and line-accurate tracebacks—no server or local Python installation required.
- **Structured 30-Day Curriculum:** Covers 30 days of Python fundamentals through advanced concepts across 4 progressive phases, complete with automated unit checks and XP rewards.
- **PyBuddy Hybrid AI & AST Tutor:**
  - **Works Free Out of the Box:** Includes a built-in local AST static analyzer that inspects your live editor code for common syntax errors, missing colons, `=` vs `==` bugs, indentation mismatches, and runtime exceptions.
  - **Optional Cloud AI:** Supports connecting your own free-tier **Google Gemini API**, **Groq API**, or a custom **Cloudflare Worker** proxy via the in-app **Settings** menu.
- **Interactive Learning Tools:**
  - **Step-by-Step Line Explorer:** Tap any line in a concept example to get a plain-English explanation of what Python executes.
  - **Daily Quick Check Quizzes:** Mini knowledge checks for each day awarding bonus XP.
  - **3-Level Progressive Hints:** Gradually unlocks a *Concept Nudge*, *Syntax Clue*, and *Code Skeleton* when you get stuck.
- **Freeform Code Playground:** Includes an open Python scratchpad preloaded with 5 runnable starter templates (*Calculator*, *Password Generator*, *Data Analyzer*, *Text RPG*, and *Fibonacci Benchmark*).
- **Offline-First Progress Tracking:** Saves completed days, XP, streaks, and unlocked achievement badges locally in the browser via `localStorage`.

---

## 📱 How to Use & Install on Mobile

You do not need an app store to install **Py30** on a phone or tablet:

1. Open the **Live App** link in your mobile browser.
2. Wait a few seconds for the top status pill to switch to **`Py 3.12 Ready`**.
3. **Install to Home Screen (Optional):**
   - **Android (Chrome):** Tap the **⋮** menu in the top-right corner and select **Add to Home screen** (or **Install app**).
   - **iPhone / iPad (Safari):** Tap the **Share** button at the bottom of the screen and select **Add to Home Screen**.

---

## 🛠️ Architecture & Tech Stack

- **Frontend:** Vanilla JavaScript (ES6+), HTML5, and Tailwind CSS in a self-contained single-file architecture (`index.html`).
- **Python Execution Engine:** Pyodide `v0.26.4` (CPython 3.12 compiled to WebAssembly).
- **Static Code Analysis:** In-browser Python `ast` module parsing for instant, zero-latency error diagnostics.
- **Hosting:** Static hosting compatible (GitHub Pages, Netlify Drop, Cloudflare Pages).

---

## 💻 Running Locally

Because `index.html` is completely self-contained, you can run it locally with any static file server:

```bash
# Clone the repository
git clone [https://github.com/TMcLaugh86/py30.git](https://github.com/TMcLaugh86/py30.git)
cd py30

# Start a quick local HTTP server with Python
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

