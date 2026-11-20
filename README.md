☁️ AZ-900 Exam Simulator

Microsoft Azure Fundamentals · 150 questions · 2 case studies · runs entirely in the browser

 
 
 

▶ Live exam: https://chrismunnps.github.io/exam-sim/az-900/

🚀 Executive summary

A free, full-length practice exam for Exam AZ-900: Microsoft Azure Fundamentals, built from the Microsoft Learn AZ-900 learning paths. It recreates the real sitting closely enough to be useful: a weighted 40-question draw, a 60-minute clock, scaled scoring against the 700 pass mark, two case studies, and six concept diagrams.

Everything runs client-side. There is no account, no install, no server, no analytics, and no network call after the page loads — scores and review history stay in the visitor's own browser.

The simulator is seven runtime files, identical in the repository and on the live site:

🌐 Live site: https://chrismunnps.github.io/exam-sim/az-900/ Served by GitHub Pages from the portfolio repo's exam-sim/az-900/ folder — the seven runtime files in this repository are exactly what is deployed.

It is an independent study tool. It is not affiliated with, endorsed by, or connected to Microsoft.

✨ Why this one is different

🧭 It behaves like the real exam. Forty questions drawn by domain weight, 90 seconds each, a running clock, flag-for-review, a question palette, and submit-on-timeout.

🧠 Explanations teach, not just score. Every item carries a rationale, a note on why each distractor is wrong, an exam tip, and the exam skill area it maps to.

🧩 Two case studies. Ten questions hang off shared scenarios — Contoso Manufacturing's migration and Fabrikam's startup growth — so you practise holding context across a case, the way the real exam does.

🖼️ Concept diagrams. Six inline SVG diagrams cover IaaS/PaaS/SaaS, regions and zones, the resource hierarchy, storage services, the inbound networking path, and the identity flow. Every diagram question also explains the concept in words.

✅ Multi-answer items are all-or-nothing. "Select two" questions are graded exactly as strictly as the exam grades them.

🔁 A spaced-review queue. Wrong answers come back on a schedule instead of disappearing, so weak domains get revisited without re-running whole exams.

🌓 Light and dark themes. A top-bar switch, remembered per browser, following the OS until you choose. Printing always forces black-on-white.

⌨️ Keyboard-first. A–E to answer, arrows to navigate, F to flag, plus a visible focus ring and a skip link.

📴 Genuinely offline. Double-click the page and it works with the network unplugged. No bundler, no local server, no runtime dependencies.

🎯 Exam at a glance

Certification
Microsoft Certified: Azure Fundamentals
Exam
AZ-900 — Microsoft Azure Fundamentals
Questions in bank
150 (140 standalone + 10 case-study)
Default attempt
40 questions, weighted by domain
Time limit
90 seconds per question — 60 minutes for the default draw
Passing score
700 / 1,000 (scaled from percentage correct)
Review
Every question after submission, with explanations and sources
Prerequisites
A browser. That is the whole list.

📚 Question bank

Domain
Standalone
Case items
Weight
IDs
Cloud concepts
40
3
25–30%
Q1–Q40
Architecture and services
55
5
35–40%
Q41–Q95
Management and governance
45
2
30–35%
Q96–Q140
Case studies
—
10
—
Q141–Q150
Total
140
10
150

Question mix: scenario-led items, least-administrative-effort choices, and ten Select two multiple-response questions, spanning recall through applied decision-making.

🗂️ Case studies

Case
Questions
Scenarios
Contoso Manufacturing Moves to Azure
Q141–Q145
Cloud model, identity, consumption pricing, region pairs, monitoring
Fabrikam Startup Growth
Q146–Q150
Elasticity, App Service, Blob storage, resilience, cost planning

🧾 Cheat sheets

Three printable one-page refreshers, one per domain, plus a single self-contained print pack. They sit in this repository alongside the simulator; only the seven runtime files are needed to run the exam.

File
Covers
04-CHEAT-SHEET-CLOUD.md
Cloud models, service models, shared responsibility, benefits, resilience vocabulary
05-CHEAT-SHEET-SERVICES.md
Regions, compute, networking, storage, identity, AI and IoT
06-CHEAT-SHEET-GOVERNANCE.md
Cost tools, RBAC, Policy, locks, monitoring, deployment, compliance
08-CHEAT-SHEETS.html
All three sheets laid out as A4 pages — open and print

Open 08-CHEAT-SHEETS.html in a browser and choose Print all three sheets. Each domain fits one A4 page at two columns, type is set for paper rather than screen, and the toolbar and background are excluded from print.

🖥️ Run it locally

The short version: download the repository and double-click index.html.

index.html        – page shell, theme bootstrap
exam.config.js    – pass mark, domains, weights, timer
questions.js      – 150 questions (the whole bank)
diagrams.js       – 6 inline SVG diagrams
app.js            – exam engine
styles.css        – shared theme, light + dark
md-loader.js      – data bootstrap and friendly failure message

No npm install. No build step. No web server. The page opens from file://, reads the bank through a plain <script> tag, and starts.

💡 Working in the authoring kit? exam-sim/index.html temporarily loads the shared engine from ../AZ-104/exam-sim/. Double-click 01-Package-Standalone.bat once to copy app.js and styles.css in and rewrite the page to local paths before publishing.

🧮 Scoring and review

📊 Scaled score. round(correct / total * 1000) — the same shape Microsoft uses in the score report. Seven out of ten is a pass.

🎆 Passing feels like passing. Clearing 700 adds a five-second fireworks overlay to the score report. It is skipped automatically when the operating system asks for reduced motion, and never appears in print.

🔍 Review everything. After submitting, filter by all / incorrect / flagged. Each item shows your answer, the correct answer, the full explanation, and the source skill area.

📄 Print or save. "Print full review" and "Print score report" produce clean paper layouts with the light palette forced, so a dark-mode session still prints readable black text.

