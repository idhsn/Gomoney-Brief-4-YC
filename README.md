## 📌 About

GoMoney is a web-based loan simulator that helps users estimate monthly payments, total interest, and total repayment across multiple loan types based on amount, term, and salary, using the standard annuity payment formula for amortizing loans.

The app guides users through selecting a loan type, entering amount, duration, and salary, then applies loan-specific interest rates to compute monthly payments and affordability versus a 40% income threshold, with clear on-screen feedback.

***

[📌 About](#-about) | [✨ Features](#-features) | [🛠️ Tech Stack](#-tech-stack) | [🧠 Loan Math](#-loan-math) | [📦 Installation](#-installation) | [🎯 Usage](#-usage) | [🗂️ Project Structure](#-project-structure) | [🧪 Test Scenarios](#-test-scenarios) | [🛡️ Accessibility](#-accessibility) | [🚀 Deployment](#-deployment) | [🗺️ Roadmap](#-roadmap) | [👥 Authors](#-authors) 

***

## ✨ Features

- 🏷️ Loan types: Maison, Appartement, Terrain, Petite entreprise, Prêt personnel.
- 🧮 Monthly payment: Annuity formula with type- and term-based rates.
- 📊 Totals: Total interest and total repayable amount with a visual share indicator.
- 🚦 Affordability: Warns if monthly payment exceeds 40% of salary (DTI guideline).
- 💾 Persistence: Saves last simulation to localStorage for quick recall.
- 🎛️ Interactive UI: Real-time updates, clear summaries, and result animations.

***

## 🛠️ Tech Stack

- UI: Tailwind CSS or Bootstrap (responsive, utility-first or component-based).
- Frontend: HTML5, vanilla JavaScript (DOM manipulation and business logic).
- Design: Figma for wireframes, flow, and rate diagrams.

***

## 🧠 Loan Math

- Payment model: Ordinary annuity for amortizing loans with fixed monthly payments.
- Monthly payment $PMT$: $PMT = P \cdot \frac{r_m(1+r_m)^n}{(1+r_m)^n - 1}$ where $P$ is principal, $r_m$ is monthly rate, $n$ is number of months.
- Totals: Total repay = $PMT \times n$; Total interest = Total repay $-$ Principal.
- Affordability: Show warning if $PMT > 0.40 \times \text{monthly salary}$.

***

## 📦 Installation

### Prerequisites

- Modern browser (Chrome, Firefox, Safari, Edge) with JavaScript enabled.

### Quick Start

- Clone the repository and open index.html in a browser.
- Ensure Tailwind/Bootstrap CSS is linked and script.js is included in index.html.
- For Tailwind: build CSS via CLI or use CDN for rapid prototyping.

***

## 🎯 Usage

- Select a loan type, enter loan amount, choose duration (years or months), and input monthly salary
- Click “Calculate” to view monthly payment, total interest, total repay, and affordability result.
- If affordable, a summary card appears; if not, a prominent warning is displayed.

***

## 🗂️ Project Structure

- index.html: Markup for inputs, results, and visual indicator.
- styles.css or tailwind.css: Theme and layout; Tailwind or Bootstrap classes.
- script.js: Rate mapping, annuity computation, validation, DOM updates, localStorage.

***

## 🧪 Test Scenarios

- Boundary: Payment equals exactly 40% of salary—should be considered accessible.
- Term variants: Short vs long terms to observe interest growth and payment changes.
- Type differences: Compare Maison vs Prêt personnel to validate rate application.

***

## 🛡️ Accessibility

- Labels and ARIA roles on inputs and result regions for screen readers.
- Keyboard navigation enabled; visible focus styles with Tailwind/Bootstrap utilities.

***

## 🚀 Deployment

- GitHub Pages: push main branch and enable Pages in repository settings.
- Ensure relative asset paths; no build step required unless Tailwind CLI is used.

***

## 👥 Authors

- Maintainer: Hatim Ibourki.

***

## 🗺️ Roadmap

- Visual charts: Interest vs principal share bar for each result.
- Rate diagram: Figma chart showing rate tiers by type and duration.
- Enhancements: Input masks, currency formatting, and downloadable PDF summaries.

***
