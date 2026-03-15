# Project Setup Guide

Welcome to the team! Follow these steps to get the project running locally.

---

## Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [Git](https://git-scm.com/)
- A code editor — we recommend [VS Code](https://code.visualstudio.com/)

---

## 1. Clone the repo

```bash
git clone https://github.com/your-org/your-repo.git
cd your-repo
```

---

## 2. Install dependencies

```bash
npm install
```

---

## 3. Set up environment variables

```bash
cp .env.example .env
```

Open `.env` and fill in the required values. Ask a teammate if you're unsure what to put there.

> Never commit `.env` to the repo.

---

## 4. Run the app

```bash
npm run dev
```

The app should now be running at [http://localhost:5173](http://localhost:5173) (or whichever port is configured).

---

## 5. Verify your setup

- [ ] App loads in the browser
- [ ] No errors in the terminal
- [ ] You can log in or reach the main page

---

## Useful scripts

| Command | What it does |
| ------- | ------------ |
| `npm run dev` | Start local dev server |
| `npm run build` | Build for production |
| `npm run lint` | Run ESLint |
| `npm test` | Run tests |

---

## Next steps

- Read [CONTRIBUTING.md](./CONTRIBUTING.md) for the Git workflow
- Read [GIT_GUIDE.md](./GIT_GUIDE.md) for branch and commit naming
- Read [FRONTEND_GUIDE.md](./FRONTEND_GUIDE.md) for coding standards
- Ask in the team chat if anything is unclear
