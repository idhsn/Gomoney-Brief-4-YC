# GoMoney – Loan Simulator

***

## 📌 About
GoMoney est une application web de simulation de prêts qui calcule la mensualité, le total des intérêts et le montant total à rembourser, selon le type de prêt, le montant, la durée et le salaire mensuel de l’utilisateur, en utilisant la formule d’annuité pour prêts amortissables.[13][14]

L’application permet de choisir le type de prêt, saisir le montant, la durée (années ou mois) et le salaire, puis applique un taux d’intérêt selon la catégorie et la durée; elle vérifie aussi l’accessibilité avec un seuil de 40% du salaire et affiche un récapitulatif clair ou un avertissement.

***

[📌 About](#-about) | [✨ Features](#-features) | [🛠️ Tech Stack](#-tech-stack) | [🧠 Loan Math](#-loan-math) | [📦 Installation](#-installation) | [🎯 Usage](#-usage) | [🗂️ Project Structure](#-project-structure) | [🧪 Test Scenarios](#-test-scenarios) | [🛡️ Accessibility](#-accessibility) | [🚀 Deployment](#-deployment) | [👥 Authors & Contributors](#-authors--contributors) | [🗺️ Roadmap](#-roadmap)

***

## ✨ Features
- 🏷️ Types de prêt: Maison, Appartement, Terrain, Petite entreprise, Prêt personnel (cash).
- 🧮 Mensualité: calcul par formule d’annuité avec taux selon type et durée.
- 📊 Totaux: intérêts cumulés et montant total à rembourser, avec indicateur visuel de la part des intérêts.
- 🚦 Accessibilité: avertissement si la mensualité dépasse 40% du salaire mensuel.
- 💾 Persistance: sauvegarde de la dernière simulation en localStorage.
- 🎛️ Interface: menu clair, mises à jour dynamiques et animation d’apparition du résultat.

***

## 🛠️ Tech Stack
- UI: Tailwind CSS ou Bootstrap pour une intégration rapide et responsive.
- Frontend: HTML5 + JavaScript vanilla (DOM, logique de calcul, validations).
- Design: Figma pour wireframes, prototype et diagrammes des taux.

***

## 🧠 Loan Math
- Modèle: annuité ordinaire pour prêts amortissables à paiements fixes.
- Mensualité $$PMT$$: $$PMT = P \cdot \frac{r_m(1+r_m)^n}{(1+r_m)^n - 1}$$ où $$P$$ = principal, $$r_m$$ = taux mensuel, $$n$$ = nombre de mois.
- Totaux: Total remboursé = $$PMT \times n$$; Intérêts = Total remboursé $$-$$ Principal.
- Seuil d’accessibilité: alerte si $$PMT > 0{.}40 \times \text{salaire mensuel}$$.

***

## 📦 Installation

### Prérequis
- Navigateur moderne (Chrome, Firefox, Safari, Edge) avec JavaScript activé.
- Optionnel: Node.js si vous utilisez Tailwind CLI ou un serveur local statique.

### Quick Start
```bash
# Cloner le dépôt
git clone https://github.com/yourusername/gomoney.git
cd gomoney

# Ouvrir le projet
# - Utiliser index.html directement dans le navigateur
# - Ou servir en local (ex: npx serve, live-server, etc.)
```
- Vérifier l’inclusion de Tailwind/Bootstrap et de script.js dans index.html.
- Avec Tailwind: utiliser la CLI ou un CDN pour prototyper rapidement.

***

## 🎯 Usage
- Sélectionner un type de prêt, saisir le montant, la durée (années ou mois) et le salaire mensuel.
- Cliquer “Calculer” pour obtenir la mensualité, les intérêts totaux, le total à rembourser et l’état d’accessibilité.
- Si non accessible, un message d’avertissement s’affiche; sinon, un récapitulatif détaillé apparaît.

***

## 🗂️ Project Structure
```
gomoney/
├─ index.html          # Formulaire, sections des résultats, indicateur visuel
├─ styles.css          # Thème/overrides ou build Tailwind
├─ script.js           # Mapping des taux, calculs, validations, DOM, localStorage
└─ assets/             # Icônes, images, favicon
```
- HTML pour la structure, composants UI avec classes Tailwind/Bootstrap.
- JS gère le mapping des taux par type et durée, la formule d’annuité et l’affichage dynamique.

***

## 🧪 Test Scenarios
- Seuil 40%: cas où $$PMT = 40\%$$ du salaire — doit rester accessible.
- Durées: comparer court terme vs long terme pour observer l’évolution intérêts/paiement.
- Types: vérifier que Maison vs Prêt personnel appliquent bien des taux distincts.

***

## 🛡️ Accessibility
- Libellés explicites, aria-live sur la zone de résultats/alertes pour lecteurs d’écran.
- Navigation clavier, focus visible et contraste suffisant via utilitaires UI.

***

## 🚀 Deployment
- GitHub Pages: pousser la branche principale puis activer Pages dans les paramètres du repo.
- Utiliser des chemins relatifs; si Tailwind CLI est utilisé, builder avant le déploiement.

***

## 👥 Authors & Contributors
- Maintainer: Hatim Ibourki.

***

## 🗺️ Roadmap
- Graphique simple: barre indiquant la part des intérêts dans le total.
- Diagramme Figma: paliers de taux par type et durée.
- Améliorations: masques de saisie, formatage monétaire, export PDF du récapitulatif.

***

## 🧩 Notes de configuration des taux
- Définir une table des taux par catégorie et par tranche de durée, par exemple: court, moyen, long terme.
- Documenter la logique d’escalade du taux selon la durée dans le README et le diagramme Figma.

***

## 📜 License
MIT — voir le fichier LICENSE.

