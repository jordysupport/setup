---
hide_support_outro: true
description: >-
  Download TUSK: a free, local-first CRM for selling websites to local businesses. Scrape real leads, grade their sites, call with real talking points, and invoice the wins.
software_schema:
  name: TUSK
  operating_system: Windows, macOS, Linux
  category: BusinessApplication
  version: 0.3.0
  download_url: https://github.com/jordysupport/tusk/archive/refs/heads/main.zip
---

<div class="tusk-hero" markdown>

<span class="kicker">TUSK / Local-First Sales CRM · Free · Open Source</span>

# The CRM that remembers every lead.

TUSK is for one specific hustle: selling websites to local businesses. It finds businesses with weak or missing websites, scores who to call first, hands you talking points built from each lead's real Google data, and tracks everything from first dial to paid invoice. All on your own computer.

[Get TUSK on GitHub](https://github.com/jordysupport/tusk){ .md-button .md-button--primary }
[Download ZIP (no git needed)](https://github.com/jordysupport/tusk/archive/refs/heads/main.zip){ .md-button }
[See the screens](#the-screens){ .md-button }

</div>

<div class="vale-preview">
  <img src="/assets/tusk/tusk-01-dashboard.webp" alt="TUSK dashboard showing lead stats, today's call and email actions, and top leads ranked by score">
</div>

<p class="vale-preview-note">Real screenshots of the current build, running on the included demo data.</p>

<div class="vale-facts">
  <div><strong>Current release</strong><span>0.3.0</span></div>
  <div><strong>Runs on</strong><span>Windows, Mac, Linux (Node 18+)</span></div>
  <div><strong>Price</strong><span>Free, MIT licensed</span></div>
  <div><strong>Your data</strong><span>One SQLite file on your machine</span></div>
</div>

## Give your agent one prompt

The fastest setup: let Claude Code, Cursor, or any coding agent install and personalize it for you.

<div class="vale-install tusk-install" markdown>
  <div><strong>Copy the prompt</strong>Use the copy button on the block below.</div>
  <div><strong>Paste it into your agent</strong>On the computer where TUSK will live.</div>
  <div><strong>Answer its questions</strong>Your name, your town, your niches. It does the rest.</div>
</div>

```text
Clone https://github.com/jordysupport/tusk and set it up for me.

1. Clone it somewhere permanent, not Downloads or a temp folder. Ask me
   where if it is not obvious.
2. Confirm Node.js 18 or newer is installed. If it is missing, tell me and
   stop.
3. Run npm install, then npm run seed, then npm run dev, and confirm the
   app loads at http://localhost:5173.
4. Open AGENT-SETUP.md in the repo and follow it from "STEP 2 - MAKE IT
   MINE" onward. It tells you what to ask me and exactly which files to
   personalize.

Rules: never handle my API keys or passwords (I type those into
server/.env myself), leave AUTO_FOLLOWUPS=false so no email ever sends
without my click, and never touch server/crm.db or server/files/ without
asking me first.
```

## Or install it by hand

Three commands after you clone or unzip it:

```bash
npm install
npm run seed
npm run dev
```

Then open `http://localhost:5173`. On Windows, double-clicking `tusk-start.cmd` does all of it, including reopening the app if it's already running. The seed step loads eight invented demo businesses so you can learn the app before real work; delete them from the Leads page whenever you're ready.

TUSK works with **zero configuration**: lead scraping returns clearly-labelled fake results and emails are logged instead of sent, so nothing real happens until you add keys. When you're ready, `.env.example` walks you through the two optional integrations: a Google Places key for real lead scraping, and SMTP for real email.

## Prefer it hosted?

TUSK is also available as a hosted service at [tuskcrm.com](https://tuskcrm.com). The free trial includes 1,000 leads and 5 searches, and the Solo plan is $9.99 a month with website audits included. Self-hosting from this page stays free forever.

## The screens

<div class="tusk-shot-grid">
  <figure>
    <img src="/assets/tusk/tusk-06-powerhour.webp" alt="Power Hour full-screen dialing session with talking points and keyboard outcomes">
    <figcaption><strong>Power Hour.</strong> A full-screen dialing session. It queues your best leads, writes talking points from their real rating, reviews, and website findings, and logs outcomes from the keyboard: 1-5 for what happened, Enter to commit, Space to skip.</figcaption>
  </figure>
  <figure>
    <img src="/assets/tusk/tusk-04-outreach.webp" alt="Outreach cockpit with call queue, phone panel, and email composer with live preview">
    <figcaption><strong>The Outreach cockpit.</strong> Queue, phone, and email on one screen. Templates fill themselves from the lead's own data, and the preview shows exactly what they'll receive before you hit Send.</figcaption>
  </figure>
  <figure>
    <img src="/assets/tusk/tusk-09-mockup.webp" alt="Mockup Studio generating a homepage draft for a salon with layout and palette switchers">
    <figcaption><strong>Mockup Studio.</strong> One click turns a lead into a personalized homepage draft: three layouts, curated palettes per trade, their real Google Business photo when one exists. Print it or screen-share it on the call.</figcaption>
  </figure>
  <figure>
    <img src="/assets/tusk/tusk-03-territory.webp" alt="Territory map with leads plotted as colored status markers around Tulsa">
    <figcaption><strong>Territory.</strong> Every lead on a dark map, colored by status. Overdue follow-ups pulse until you deal with them.</figcaption>
  </figure>
  <figure>
    <img src="/assets/tusk/tusk-07-lead-score.webp" alt="Lead score breakdown showing opportunity, review volume, reputation, and contact reachability">
    <figcaption><strong>Honest scoring.</strong> Every lead is ranked 0-100 from how broken their web presence is, how established the business is, and whether you can actually reach them. The math is shown, not hidden.</figcaption>
  </figure>
  <figure>
    <img src="/assets/tusk/tusk-05-pipeline.webp" alt="Pipeline kanban board with stage columns and a proportional funnel bar">
    <figcaption><strong>Pipeline.</strong> Drag conversations through stages. Empty stages collapse to rails so the whole board fits on one screen.</figcaption>
  </figure>
</div>

## A normal day in TUSK

<div class="path-strip">
  <div><span class="step-no">01</span>Scrape a niche in your town</div>
  <div><span class="step-no">02</span>Let it grade their websites</div>
  <div><span class="step-no">03</span>Run a Power Hour</div>
  <div><span class="step-no">04</span>Send the mockup or audit</div>
  <div><span class="step-no">05</span>Invoice the yes</div>
</div>

The pitch TUSK is built around: offer a free homepage mockup up front, so the business judges you on the result instead of the promise. The Mockup Studio makes that a one-click promise to keep.

## What else is inside

<div class="grid cards" markdown>

-   **Site audits in owner language**

    Each lead's website is graded A to F on things owners feel: no way to contact them, broken on phones, slow, insecure. Sites that block checkers get an honest "?" instead of a fake F.

-   **Email that fills itself**

    Templates pull the lead's name, town, rating, and the single worst finding from their own site scan. You approve every send; nothing goes out on its own.

-   **Clients, documents, invoices**

    Won leads become clients with projects, file attachments, and numbered invoices from Draft to Paid, with your payment instructions on every one.

-   **A one-click Excel workbook**

    Dashboard KPIs, every lead with its grade, and clients with invoice totals: three polished sheets, ready to print or email.

</div>

## Private by construction

- Everything runs on your computer. No account, no cloud, no telemetry.
- Your entire CRM is one SQLite file (`server/crm.db`). Copy it and you've made a backup.
- Emails only send after you click Send, and the auto-follow-up job stays off unless you deliberately turn it on.
- The optional Google and SMTP keys live in your local `.env` and are never bundled or transmitted anywhere else.

## Free, with a tip jar

TUSK is MIT licensed and free forever. If it lands you a client, [a Ko-fi tip](https://ko-fi.com/support_jordy) keeps it maintained and growing.

[Get TUSK on GitHub](https://github.com/jordysupport/tusk){ .md-button .md-button--primary }
[Tip on Ko-fi](https://ko-fi.com/support_jordy){ .md-button }
