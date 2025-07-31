# 🧩 Frontend Web – Git Workflow & Conventions

This repository contains the web frontend application.

---

## 🚀 Git Strategy

We use **Trunk-Based Development** with **GitHub Flow**.

### 📌 Branches
- `main`: Production-ready, auto-deployed.
- `feature/*`: New features (short-lived).
- `fix/*`: Bugfixes.
- `infra/*`: Optional for deployment scripts or env setup.

---

## ✅ GitHub Flow

1. `git checkout -b feature/<short-description>`
2. Push frequently
3. Open PR to `main`
4. Run CI (lint, test, build, preview deployment)
5. Code review & squash merge
6. Auto-deploy to production on `main`

---

## 🔐 Secrets

Secrets like API keys are injected via:
- GitHub Actions Environments
- `.env` (local only, in `.gitignore`)
- AWS Parameter Store (Secrets Manager after migration)

---

## 📦 CI/CD

GitHub Actions runs:
- Linting (`eslint`, `prettier`)
- Tests (Jest, Cypress)
- Build (Vite/Webpack)
- K8s static container

---

## 🧠 Notes

- Keep PRs small and reviewed.
- Prefer functional, atomic commits.
- Use `.env.example` for local setup reference.
