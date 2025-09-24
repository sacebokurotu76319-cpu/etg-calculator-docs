# ETG Calculator Online

A free, realistic **EtG (ethyl glucuronide) detection window helper**.  
This project powers the website **[etgcalculatoronline.com](https://etgcalculatoronline.com/)** and provides an educational tool to estimate a **possible time range** when EtG might be detectable after alcohol consumption.

> **Important disclaimer**  
> This calculator is **for education only** and does **not** provide medical, legal, or laboratory advice. Actual detection windows vary widely between people and testing methods. Always defer to your clinician, testing facility, and the official instructions for your test.

---

## 🔗 Live
- **Website:** https://etgcalculatoronline.com/

If you are reading this on GitHub, the repository contains the calculator’s source and documentation so that anyone can review, run locally, or self‑host.

---

## ✨ What it does
- Estimates a **conservative detection window** for EtG based on typical ranges reported in public literature and common heuristics.
- Lets you enter simple inputs (e.g., number of standard drinks, time since last drink) and returns a **rough timeframe** rather than a single “yes/no” answer.
- Explains **assumptions and limits** so users understand the result is an approximation, not a guarantee.
- Works entirely in the browser (no account required).

---

## 🧠 How it works (high‑level)
This tool uses a heuristic model to produce a **range**. It intentionally biases toward a **more cautious/longer** detection window where uncertainty exists. The logic aims to be transparent and simple enough to audit:

- Inputs (examples):
  - Count of standard drinks (or an approximate alcohol amount).
  - Time since last drink ended.
  - Optional context (sex, body weight, hydration, sleep) if available.  
- Output:
  - A **range** (e.g., “EtG may be detectable for approximately _X–Y hours_ from the last drink”) with a textual explanation.
- Design principles:
  - **No laboratory prediction.** This is not a clinical tool and does not replace a lab test.
  - **Privacy‑first.** All calculations can be performed locally in the browser.
  - **Transparency.** The README documents assumptions; comments in code explain each step.

> If you are contributing, please keep the code readable and keep comments close to the formulas/heuristics so users can follow the reasoning.

---

## 🛠 Run locally

### Option A — static (no build step)
If the project is plain HTML/CSS/JS:
```bash
git clone https://github.com/<your-org-or-user>/<your-repo>.git
cd <your-repo>
# Open index.html in your browser, or serve the folder:
python3 -m http.server 5173
# visit http://localhost:5173
```

### Option B — Node tooling (if applicable)
If the repo uses a bundler (Vite/Next/CRA/etc.), typical commands will be:
```bash
# install dependencies
npm install

# dev server
npm run dev

# production build
npm run build
npm run preview
```
> Check `package.json` for the exact scripts used by this repository.

---

## 📦 Deploy / self‑host
Any static host will work (GitHub Pages, Netlify, Vercel, Cloudflare Pages, S3, nginx).  
If your build produces a `dist/` folder, deploy that directory.

---

## 🔒 Privacy
- The calculator can run fully client‑side.  
- We avoid collecting personally identifiable information in the app.  
- If analytics are enabled, keep them **privacy‑respecting** and documented here (e.g., disable IP logging, use cookieless modes).

---

## ⚠️ Assumptions & limitations
- EtG detection depends on **many factors**: test type and cutoff level, hydration, metabolism, amount and pattern of drinking, health, and more.
- This tool provides **approximate ranges** only. It cannot determine individual outcomes and must **not** be used to make medical or legal decisions.
- Cutoffs and lab procedures vary by provider and over time; always check your lab’s documentation.

---

## 🧩 Embedding
You can link to the public site or embed the calculator in your documentation as an iframe:
```html
<iframe src="https://etgcalculatoronline.com/" width="100%" height="640" style="border:0;" loading="lazy"></iframe>
```
Please ensure embedding respects your organization’s policies and this project’s license.

---

## 🤝 Contributing
Contributions are welcome! If you improve clarity, math/assumptions, or accessibility:
1. Fork & create a feature branch.
2. Make changes with clear comments around formulas/heuristics.
3. Open a Pull Request with a concise description and screenshots (if UI).

Please avoid adding external trackers or heavy dependencies without discussion.

---

## 📄 License
MIT. See `LICENSE` for details.

---

## 👋 Maintainer & contact
**ETG Calculator Online** — maintained by the project team.  
Primary contact: **support@etgcalculatoronline.com**  
(If you need a press or legal contact, open an issue or email first.)

---

## FAQ

**Is this medical advice?**  
No. The calculator is only an educational helper that provides rough ranges.

**Why give a range instead of a single result?**  
True detection windows vary between individuals and labs. Ranges communicate uncertainty better and reduce false confidence.

**Can I use this for court / compliance?**  
No. Always defer to official lab testing and professional guidance.

**Does the site store my data?**  
The client‑side calculator does not need to store personal inputs; check the code for details. If a future version introduces optional saving, it will be documented here.

---

If you use or adapt this project, please consider linking back to **https://etgcalculatoronline.com/** so others can find the original tool and documentation.
