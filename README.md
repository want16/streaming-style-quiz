# Find Your Streaming Style — Landing Prototype

This is a single‑file, deploy‑ready prototype (HTML + Tailwind CDN + vanilla JS). It includes:
- Minimal 1‑3‑1 hero
- **Find Your Streaming Style** quiz (modal)
- Result personas with quick recommendations

---

## 🚀 Deploy (Baby Steps)

### Option A — **GitHub → Vercel** (no terminal)
1. Go to **github.com** → **New repository** → Name it `streaming-style-quiz` → Click **Create**.
2. On your computer, unzip the file you downloaded from ChatGPT.
3. Drag **`index.html`** into the repo on GitHub and **Commit changes**.
4. Go to **vercel.com** → **New Project** → **Import Git Repository** → pick `streaming-style-quiz`.
5. **Framework Preset:** *Other*. Build command: *(leave empty)*. Output directory: *(leave empty)*.
6. Click **Deploy** → Vercel gives you a live URL.

### Option B — **Terminal (Git + Vercel CLI)**
1. Install Node.js (if you don’t have it).
2. Install the Vercel CLI:
   ```bash
   npm i -g vercel
   ```
3. Log in to Vercel:
   ```bash
   vercel login
   ```
4. Create a project folder and add the file:
   ```bash
   mkdir streaming-style-quiz && cd $_
   # Put index.html in this folder (copy/paste or save)
   git init
   git add index.html
   git commit -m "init: streaming style quiz"
   ```
5. Push to GitHub:
   ```bash
   gh repo create streaming-style-quiz --public --source=. --remote=origin --push
   # If you don’t have GitHub CLI, create an empty repo on github.com and then:
   git remote add origin https://github.com/<your-username>/streaming-style-quiz.git
   git push -u origin main
   ```
6. Deploy from the folder:
   ```bash
   vercel --name streaming-style-quiz
   ```
   - When asked for build settings, choose **`Other`** and accept defaults.
   - Vercel prints a URL — that’s your site.

### Option C — **VS Code (with Git + Vercel)**
1. Open **VS Code** → **File → Open Folder…** → select your project folder.
2. Create a file `index.html` and paste the code from this repo.
3. In the **Source Control** tab → **Initialize Repository** → **Commit**.
4. Click **Publish to GitHub** (or run `Git: Publish` in the Command Palette).
5. Install **Vercel** extension (optional) or run `vercel` in **Terminal** inside VS Code.
6. Follow the prompts to deploy. Done!

---

## 🧪 Customize the Quiz
- Change persona names or recommendations in the `styles` object.
- Add/remove questions in the `quiz` array — each option maps to a persona key.
- Swap the hero image by replacing the Unsplash URL near the top.

## 🛟 Notes
- This uses **Tailwind via CDN**, so no build step is required.
- All interactivity is **vanilla JavaScript** — one file, easy to host anywhere.
