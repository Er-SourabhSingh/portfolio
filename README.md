# Sourabh Singh — Personal Portfolio

![CI/CD](https://github.com/Er-SourabhSingh/Portfolio/actions/workflows/ci-cd.yml/badge.svg)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue?logo=github)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

A fully responsive personal portfolio website built with pure HTML, CSS, and JavaScript. Designed using the [vCard portfolio](https://github.com/codewithsadee/vcard-personal-portfolio) layout concept, enhanced with modern visual effects and automated CI/CD deployment.

🌐 **Live Site:** [https://er-sourabhsingh.github.io/Portfolio](https://er-sourabhsingh.github.io/Portfolio)

---

## Features

- Responsive design — works on mobile, tablet, and desktop (up to 1920px)
- Animated aurora background with glassmorphism cards
- Spinning gradient border avatar with photo/initials fallback
- Animated skill progress bars
- Filterable portfolio section (Manual Testing / Automation Testing)
- Contact form powered by [Web3Forms](https://web3forms.com) — messages delivered to Gmail
- Tab-based navigation (About, Resume, Portfolio, Contact)
- Automated CI/CD via GitHub Actions

---

## Tech Stack

| Category | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Icons | Ionicons 5 |
| Fonts | Google Fonts — Poppins |
| Contact Form | Web3Forms |
| Hosting | GitHub Pages |
| CI/CD | GitHub Actions |

---

## Project Structure

```
Portfolio/
├── .github/
│   └── workflows/
│       └── ci-cd.yml    # GitHub Actions CI/CD pipeline
├── img/
│   └── My_image.png     # Profile photo (add your photo here)
├── index.html           # Main portfolio (HTML + CSS + JS)
└── README.md
```

---

## CI/CD Pipeline

Every push to `main` triggers the GitHub Actions pipeline:

```
Push to main
     │
     ▼
┌─────────────┐        ┌──────────────────────┐
│  CI: Validate│  pass  │  CD: Deploy to       │
│  HTML5 syntax│ ──────▶│  GitHub Pages        │
└─────────────┘        └──────────────────────┘
```

- **CI** — validates `index.html` on every push and pull request
- **CD** — auto-deploys to GitHub Pages only when CI passes on `main`
- Pull requests are validated but **not** deployed

---

## Setup & Deployment

### 1 — Fork / Clone this repository

```bash
git clone https://github.com/Er-SourabhSingh/Portfolio.git
cd Portfolio
```

### 2 — Set up the contact form

1. Go to [web3forms.com](https://web3forms.com)
2. Enter your email → click **Get Access Key**
3. Open `index.html` and replace:
   ```js
   const WEB3FORMS_ACCESS_KEY = "your-access-key-here";
   ```

### 3 — Enable GitHub Pages with GitHub Actions

1. Push the repo to GitHub
2. Go to **Settings** → **Pages**
3. Under **Source** → select **GitHub Actions**
4. Push any change to `main` — the pipeline deploys automatically

### 4 — Add your profile photo

Upload any image to `img/My_image.png` in the repository.  
The portfolio detects it automatically — no code changes needed.

---

## License

This project is open source and available under the [MIT License](LICENSE).
