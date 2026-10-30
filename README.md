# AdvacePlaywrightFramework

Repository for the **Advance Playwright Framework 3x** — an end-to-end test automation framework built on **Playwright + TypeScript**.

- **GitHub:** https://github.com/Shashirehp/AdvacePlaywrightFramework
- **Branch:** `main`
- **Remote:** `origin` → `https://github.com/Shashirehp/AdvacePlaywrightFramework.git`

## What was done

- Verified the local repository state and remote configuration.
- Confirmed the code is committed and in sync with `origin/main`.
- Pushed the repository contents to GitHub (`main` → `349908c Initial commit`).

## Repository layout

```
AdvacePlaywrightFramework
├── .commandcode/              → Command Code session config and learned preferences
└── AdvancePlaywrightFramework3x/   → The Playwright + TypeScript framework
    ├── src/                   → pages, fixtures, tests, config, utils, test data
    ├── docs/
    ├── rules/
    ├── learnings/
    ├── .github/               → CI workflow
    ├── .env.example
    ├── package.json
    ├── playwright.config.ts
    └── tsconfig.json
```

## The framework

The full framework documentation lives in
[`AdvancePlaywrightFramework3x/README.md`](AdvancePlaywrightFramework3x/README.md).
It covers the tech stack, folder structure, page objects, custom fixtures, visual
steps, environment configuration, reporting, and how to run the tests.

## Getting started

```bash
cd AdvancePlaywrightFramework3x
npm ci
npx playwright install
cp .env.example .env      # then edit .env with your values
npx playwright test
```
