<div align="center">

# ☁️ AZ-900 Exam Simulator

[![Live exam](https://img.shields.io/badge/%E2%96%B6%20Take%20the%20exam-chrismunnps.github.io-0d9488?style=for-the-badge)](https://chrismunnps.github.io/exam-sim/az-900/)
[![Questions](https://img.shields.io/badge/questions-150-2563eb?style=for-the-badge)](#-question-bank)
[![Pass mark](https://img.shields.io/badge/pass%20mark-700%20%2F%201000-7c3aed?style=for-the-badge)](#-scoring-and-review)
[![Exam time](https://img.shields.io/badge/exam%20time-60%20minutes-f59e0b?style=for-the-badge)](#-exam-at-a-glance)
[![Case studies](https://img.shields.io/badge/case%20studies-2-0891b2?style=for-the-badge)](#-case-studies)
[![Offline](https://img.shields.io/badge/offline-double--click-16a34a?style=for-the-badge)](#-run-it-locally)

### Microsoft Azure Fundamentals · 150 questions · 2 case studies · runs entirely in the browser

**▶ Live exam: https://chrismunnps.github.io/exam-sim/az-900/**

</div>

---

## 🚀 Executive summary

A free, full-length practice exam for **Exam AZ-900: Microsoft Azure Fundamentals**, built from the Microsoft Learn AZ-900 learning paths. It recreates the real sitting closely enough to be useful: a weighted 40-question draw, a 60-minute clock, scaled scoring against the 700 pass mark, two case studies, and six concept diagrams.

Everything runs client-side. There is no account, no install, no server, no analytics, and no network call after the page loads — scores and review history stay in the visitor's own browser.

The simulator is seven runtime files, identical in the repository and on the live site:

> **🌐 Live site: https://chrismunnps.github.io/exam-sim/az-900/**
> Served by GitHub Pages from the portfolio repo's `exam-sim/az-900/` folder — the seven runtime files in this repository are exactly what is deployed.

It is an independent study tool. It is not affiliated with, endorsed by, or connected to Microsoft.

---

## ✨ Why this one is different

🧭 **It behaves like the real exam.** Forty questions drawn by domain weight, 90 seconds each, a running clock, flag-for-review, a question palette, and submit-on-timeout.

🧠 **Explanations teach, not just score.** Every item carries a rationale, a note on why each distractor is wrong, an exam tip, and the exam skill area it maps to.

🧩 **Two case studies.** Ten questions hang off shared scenarios — Contoso Manufacturing's migration and Fabrikam's startup growth — so you practise holding context across a case, the way the real exam does.

🖼️ **Concept diagrams.** Six inline SVG diagrams cover IaaS/PaaS/SaaS, regions and zones, the resource hierarchy, storage services, the inbound networking path, and the identity flow. Every diagram question also explains the concept in words.

✅ **Multi-answer items are all-or-nothing.** "Select two" questions are graded exactly as strictly as the exam grades them.

🔁 **A spaced-review queue.** Wrong answers come back on a schedule instead of disappearing, so weak domains get revisited without re-running whole exams.

🌓 **Light and dark themes.** A top-bar switch, remembered per browser, following the OS until you choose. Printing always forces black-on-white.

⌨️ **Keyboard-first.** `A`–`E` to answer, arrows to navigate, `F` to flag, plus a visible focus ring and a skip link.

📴 **Genuinely offline.** Double-click the page and it works with the network unplugged. No bundler, no local server, no runtime dependencies.

---

## 🎯 Exam at a glance

| | |
|---|---|
| **Certification** | Microsoft Certified: Azure Fundamentals |
| **Exam** | AZ-900 — Microsoft Azure Fundamentals |
| **Questions in bank** | 150 (140 standalone + 10 case-study) |
| **Default attempt** | 40 questions, weighted by domain |
| **Time limit** | 90 seconds per question — 60 minutes for the default draw |
| **Passing score** | 700 / 1,000 (scaled from percentage correct) |
| **Review** | Every question after submission, with explanations and sources |
| **Prerequisites** | A browser. That is the whole list. |

---

## 📚 Question bank

| Domain | Standalone | Case items | Weight | IDs |
|---|---:|---:|---|---|
| Cloud concepts | 40 | 3 | 25–30% | Q1–Q40 |
| Architecture and services | 55 | 5 | 35–40% | Q41–Q95 |
| Management and governance | 45 | 2 | 30–35% | Q96–Q140 |
| Case studies | — | 10 | — | Q141–Q150 |
| **Total** | **140** | **10** | | **150** |

**Question mix:** scenario-led items, least-administrative-effort choices, and ten `Select two` multiple-response questions, spanning recall through applied decision-making.

### 🗂️ Case studies

| Case | Questions | Scenarios |
|---|---|---|
| Contoso Manufacturing Moves to Azure | Q141–Q145 | Cloud model, identity, consumption pricing, region pairs, monitoring |
| Fabrikam Startup Growth | Q146–Q150 | Elasticity, App Service, Blob storage, resilience, cost planning |

---

## 🧾 Cheat sheets

Three printable one-page refreshers, one per domain, plus a single self-contained print pack. They sit in this repository alongside the simulator; only the seven runtime files are needed to run the exam.

| File | Covers |
|---|---|
| `04-CHEAT-SHEET-CLOUD.md` | Cloud models, service models, shared responsibility, benefits, resilience vocabulary |
| `05-CHEAT-SHEET-SERVICES.md` | Regions, compute, networking, storage, identity, AI and IoT |
| `06-CHEAT-SHEET-GOVERNANCE.md` | Cost tools, RBAC, Policy, locks, monitoring, deployment, compliance |
| `08-CHEAT-SHEETS.html` | All three sheets laid out as A4 pages — open and print |

Open `08-CHEAT-SHEETS.html` in a browser and choose **Print all three sheets**. Each domain fits one A4 page at two columns, type is set for paper rather than screen, and the toolbar and background are excluded from print.

---

## 🖥️ Run it locally

**The short version:** download the repository and double-click `index.html`.

```text
index.html        – page shell, theme bootstrap
exam.config.js    – pass mark, domains, weights, timer
questions.js      – 150 questions (the whole bank)
diagrams.js       – 6 inline SVG diagrams
app.js            – exam engine
styles.css        – shared theme, light + dark
md-loader.js      – data bootstrap and friendly failure message
```

No `npm install`. No build step. No web server. The page opens from `file://`, reads the bank through a plain `<script>` tag, and starts.

> 💡 **Working in the authoring kit?** `exam-sim/index.html` temporarily loads the shared engine from `../AZ-104/exam-sim/`. Double-click `01-Package-Standalone.bat` once to copy `app.js` and `styles.css` in and rewrite the page to local paths before publishing.

---

## 🧮 Scoring and review

📊 **Scaled score.** `round(correct / total * 1000)` — the same shape Microsoft uses in the score report. Seven out of ten is a pass.

🎆 **Passing feels like passing.** Clearing 700 adds a five-second fireworks overlay to the score report. It is skipped automatically when the operating system asks for reduced motion, and never appears in print.

🔍 **Review everything.** After submitting, filter by all / incorrect / flagged. Each item shows your answer, the correct answer, the full explanation, and the source skill area.

📄 **Print or save.** "Print full review" and "Print score report" produce clean paper layouts with the light palette forced, so a dark-mode session still prints readable black text.

💾 **Resume safe.** An in-progress attempt is saved on every change. Close the tab, come back, and the clock and answers are where you left them.

---

## 🔐 Privacy

Everything is local. The simulator writes four keys to `localStorage` and nothing else:

| Key | Holds |
|---|---|
| `az900-sim:attempt` | The in-progress attempt, for resume |
| `az900-sim:settings` | Draw size, timer, instant-feedback preference |
| `az900-sim:srs` | Spaced-review scheduling data |
| `az900-sim:theme` | Light or dark choice |

No cookies, no requests to third parties, no telemetry. Clearing site data for the page resets the simulator completely.

---

## ♿ Accessibility

- Full keyboard operation, including `A`–`E` (or `1`–`5`) answer keys and arrow navigation.
- Semantic landmarks, a skip link, and a polite live region for toasts.
- Visible focus rings and readable contrast in both themes.
- `prefers-reduced-motion` disables the fireworks and shortens transitions.
- Diagrams are hidden from assistive technology; every diagram question restates the concept in prose.

---

## 🛠️ For maintainers

The repository ships the built simulator and the printable cheat sheets. Packaging scripts and batch files live in the working kit, not here.

Scope, bank counts, case coverage, and the diagram map are recorded in `00-EXAM-BLUEPRINT.md`.

**Pipeline**

```text
exam-sim\            ──01-Package-Standalone.bat──▶  local app.js + styles.css
exam-sim\            ──02-Make-Web-Copy.bat───────▶  publish\az-900\ (the upload folder)
```

**Publishing**

1. Run `01-Package-Standalone.bat`, then `02-Make-Web-Copy.bat`.
2. Copy the seven files from `publish\az-900\` into the portfolio repo at `exam-sim/az-900/`.
3. Push to `main`; GitHub Pages deploys automatically.
4. Live at `https://chrismunnps.github.io/exam-sim/az-900/`.

**Bank format** — the helper at the top of `questions.js` keeps items compact:

```js
Q(51, 'architecture', 'Resource groups',
  'A team wants to delete a temporary dev environment in one action. What should it use?',
  ['Put all the resources in one resource group and delete the group',
   'Delete each resource individually',
   'Move the resources to another subscription',
   'Create a management group for the environment'],
  ['A'],
  'Explanation with **bold** and - bullet notes.\n\n**Exam tip:** ...',
  'Describe Azure architecture and services - Describe core architectural components of Azure',
  { diagram: 'resource-hierarchy' })
```

The bank has been checked for 150 unique IDs, four options each, valid answer letters, existing case and diagram keys, and multi-answer stems that say "select two". It intentionally avoids volatile numbers such as prices and quotas.

**A note on drag-and-drop:** the shared engine grades selections, not orderings, so AZ-900 drag-and-drop objectives are represented as multiple-response items rather than a simulated drag interface.

---

## ⚠️ Disclaimer

Unofficial study material built from publicly available Microsoft Learn content. Not affiliated with or endorsed by Microsoft. Exam objectives and product behaviour change; verify the current skills measured on Microsoft Learn before sitting the exam. Facts snapshot: **November 2026**.

<div align="center">

**[▶ Start practising](https://chrismunnps.github.io/exam-sim/az-900/)** · [Microsoft Learn AZ-900](https://learn.microsoft.com/en-us/credentials/certifications/azure-fundamentals/)

</div>
