## 📌 About

GoMoney is a web-based loan simulator that helps users estimate monthly payments, total interest, and total repayment across multiple loan types based on amount, term, and salary, using the standard annuity payment formula for amortizing loans.[^3][^4]

The app guides users through selecting a loan type, entering amount, duration, and salary, then applies loan-specific interest rates to compute monthly payments and affordability versus a 40% income threshold, with clear on-screen feedback.[^5][^6]

***

[📌 About](#-about) | [✨ Features](#-features) | [🛠️ Tech Stack](#-tech-stack) | [🧠 Loan Math](#-loan-math) | [📦 Installation](#-installation) | [🎯 Usage](#-usage) | [🗂️ Project Structure](#-project-structure) | [🧪 Test Scenarios](#-test-scenarios) | [🛡️ Accessibility](#-accessibility) | [🚀 Deployment](#-deployment) | [🗺️ Roadmap](#-roadmap) | [👥 Authors](#-authors) [^7][^8]

***

## ✨ Features

- 🏷️ Loan types: Maison, Appartement, Terrain, Petite entreprise, Prêt personnel.[^9]
- 🧮 Monthly payment: Annuity formula with type- and term-based rates.[^10]
- 📊 Totals: Total interest and total repayable amount with a visual share indicator.[^3]
- 🚦 Affordability: Warns if monthly payment exceeds 40% of salary (DTI guideline).[^5]
- 💾 Persistence: Saves last simulation to localStorage for quick recall.[^6]
- 🎛️ Interactive UI: Real-time updates, clear summaries, and result animations.[^11]

***

## 🛠️ Tech Stack

- UI: Tailwind CSS or Bootstrap (responsive, utility-first or component-based).[^12]
- Frontend: HTML5, vanilla JavaScript (DOM manipulation and business logic).[^9]
- Design: Figma for wireframes, flow, and rate diagrams.[^9]

***

## 🧠 Loan Math

- Payment model: Ordinary annuity for amortizing loans with fixed monthly payments.[^13]
- Monthly payment $PMT$: $PMT = P \cdot \frac{r_m(1+r_m)^n}{(1+r_m)^n - 1}$ where $P$ is principal, $r_m$ is monthly rate, $n$ is number of months.[^10]
- Totals: Total repay = $PMT \times n$; Total interest = Total repay $-$ Principal.[^3]
- Affordability: Show warning if $PMT > 0.40 \times \text{monthly salary}$.[^5]

***

## 📦 Installation

### Prerequisites

- Modern browser (Chrome, Firefox, Safari, Edge) with JavaScript enabled.[^6]
- Optional: Node.js for local static server and Tailwind CLI workflow.[^12]


### Quick Start

- Clone the repository and open index.html in a browser.[^2]
- Ensure Tailwind/Bootstrap CSS is linked and script.js is included in index.html.[^12]
- For Tailwind: build CSS via CLI or use CDN for rapid prototyping.[^12]

***

## 🎯 Usage

- Select a loan type, enter loan amount, choose duration (years or months), and input monthly salary.[^9]
- Click “Calculate” to view monthly payment, total interest, total repay, and affordability result.[^4]
- If affordable, a summary card appears; if not, a prominent warning is displayed.[^5]

***

## 🗂️ Project Structure

- index.html: Markup for inputs, results, and visual indicator.[^9]
- styles.css or tailwind.css: Theme and layout; Tailwind or Bootstrap classes.[^12]
- script.js: Rate mapping, annuity computation, validation, DOM updates, localStorage.[^3]

***

## 🧪 Test Scenarios

- Boundary: Payment equals exactly 40% of salary—should be considered accessible.[^5]
- Term variants: Short vs long terms to observe interest growth and payment changes.[^3]
- Type differences: Compare Maison vs Prêt personnel to validate rate application.[^10]

***

## 🛡️ Accessibility

- Labels and ARIA roles on inputs and result regions for screen readers.[^6]
- Keyboard navigation enabled; visible focus styles with Tailwind/Bootstrap utilities.[^12]

***

## 🚀 Deployment

- GitHub Pages: push main branch and enable Pages in repository settings.[^2]
- Ensure relative asset paths; no build step required unless Tailwind CLI is used.[^12]

***

## 👥 Authors

- Maintainer: Hatim Ibourki.[^2]

***

## 🗺️ Roadmap

- Visual charts: Interest vs principal share bar for each result.[^3]
- Rate diagram: Figma chart showing rate tiers by type and duration.[^9]
- Enhancements: Input masks, currency formatting, and downloadable PDF summaries.[^6]

***
