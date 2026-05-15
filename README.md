<div align="center">

# 📖 LeadGen.js Documentation

**The official documentation site for [LeadGen.js](https://nilegazer00.github.io/NileGazer00-js-leadmachine/)**

A lightweight, zero-dependency JavaScript library for capturing leads directly to Google Sheets — no backend required.

[![Live Docs](https://img.shields.io/badge/docs-live-brightgreen?style=flat-square&logo=github&labelColor=1a1a1a)](https://js-leadmachine.js.org)
[![JS.ORG](https://img.shields.io/badge/hosted_on-js.org-FFE70B?style=flat-square&labelColor=1a1a1a)](https://js-leadmachine.js.org)
[![LeadGen.js](https://img.shields.io/badge/library-leadgen.js-f7df1e?style=flat-square&logo=javascript&labelColor=1a1a1a)](https://github.com/NileGazer00/leadgen.js)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square&labelColor=1a1a1a)](https://github.com/NileGazer00/leadgen.js/blob/main/LICENSE)

</div>

---

## 🌐 Live Site

The documentation is live at:

- **[js-leadmachine.js.org](https://js-leadmachine.js.org)** — custom domain via JS.ORG
- **[nilegazer00.github.io/NileGazer00-js-leadmachine](https://nilegazer00.github.io/NileGazer00-js-leadmachine/)** — GitHub Pages fallback

---

## 📋 About This Repository

This repository contains the **documentation website** for [LeadGen.js](https://nilegazer00.github.io/), a zero-dependency vanilla JavaScript library that captures form submissions and stores lead data directly in Google Sheets without any backend infrastructure.

The documentation is built as a **single-page static site** (`index.html`) with no build tools, frameworks, or dependencies — keeping it fast, lightweight, and easy to maintain, just like LeadGen.js itself.

### What You'll Find in the Docs

| Section | Description |
|---------|-------------|
| **Getting Started** | Step-by-step guide from HTML form creation to first submission |
| **Installation** | CDN, local file, ES Module, and npm/bundler integration options |
| **Google Sheets Setup** | Complete guide to creating and deploying the Google Apps Script web app |
| **API Reference** | Full documentation for `LeadGen.init()`, `.setTheme()`, `.getAnalytics()`, `.validateForm()`, `.destroy()`, and `.calculateNeeded()` |
| **Examples** | Working code for basic forms, React, Vue 3, multi-step forms, and dark mode toggles |
| **Configuration** | All options: `formId`, `sheetUrl`, `theme`, `validate`, `debug`, callbacks, and more |
| **Troubleshooting** | Fixes for CORS errors, 401 issues, missing data, page reloads, and validation problems |
| **FAQ** | Answers on security, rate limits, multi-sheet support, spam protection, and file uploads |
| **Contributing** | Guidelines for bug reports, feature requests, pull requests, and code style |

---

## 🚀 Quick Start

If you're looking to **use LeadGen.js** in your project, head straight to the live docs:

👉 **[js-leadmachine.js.org](https://nilegazer00.github.io/NileGazer00-js-leadmachine/)**

The simplest way to get started:

```html
<form id="my-lead-form">
  <input type="text" name="name" placeholder="Your Name" required>
  <input type="email" name="email" placeholder="Email" required>
  <button type="submit">Submit</button>
</form>

<script src="https://cdn.jsdelivr.net/gh/NileGazer00/leadgen.js/leadgen.js"></script>
<script>
  LeadGen.init({
    formId: "my-lead-form",
    sheetUrl: "YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL"
  });
</script>
