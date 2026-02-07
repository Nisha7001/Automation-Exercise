# 🧪 Playwright Testing Guide

A quick reference for running Playwright tests with various configurations and environment setups.

---

## 🚀 Common Commands

npm run test your-test-file.spec.js

## Staging Env

npm run test:stage your-test-file.spec.js

### 🎥 Record Tests

```bash
npx playwright codegen
```

### 🧪 Run Tests in UI Mode

```bash
npx playwright test --ui
```

### 🔍 Run a Specific Test File

```bash
npx playwright test your-test-file.spec.js
```

### 🖥️ Run Tests with GUI

```bash
npx playwright test --headed 
```

> **Note:** Adding `--workers=3` helps avoid rate limiting during test runs.

---

## 🔐 .env Configuration

Set the following environment variables in your `.env` file:

```env
EMAIL=your_email@example.com
PASSWORD=your_password

INTERNAL_URL=https://internal.openscreen[-dev|-staging].com
DASHBOARD_URL=https://app.openscreen[-dev|-staging].com
OSPRO_URL=https://ospro[-d|-s].co

APP_URL=https://internal.[dv|st|v2].os-track.com
APP_ORIGIN=https://app.[dev|staging].os-track.com

ACCOUNT_ID=your_core_account_id
APP_ID=your_track_app_id
```

> Replace placeholders with your actual environment values.

---

## 📸 Test Recording & Screenshots

To enable screenshots or video recording, configure your `playwright.config.js` or specify in individual tests using
`test.use`.

```js
use: {
      // screenshot: 'only-on-failure', // options: 'on', 'off', 'only-on-failure'
      // video: 'on',                   // options: 'on', 'off', 'only-on-failure'
}
```

Uncomment and adjust based on your use case.
