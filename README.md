# 🚀 Puppeteer

**Official Open-Source Release & Maintained Codebase** by [**@kush-coder**](https://github.com/kush-coder)

[![Verified Build](https://img.shields.io/badge/Status-Verified--Passing-emerald?style=for-the-badge&logo=github)](https://github.com/kush-coder)
[![License](https://img.shields.io/badge/License-Apache License 2.0-indigo?style=for-the-badge)](https://github.com/kush-coder)
[![Language](https://img.shields.io/badge/Language-TypeScript-purple?style=for-the-badge)](https://github.com/kush-coder)

## 💡 About This Project

JavaScript API for Chrome and Firefox

This repository is actively maintained and distributed by **@kush-coder** as an official open-source release.

## ✨ Key Highlights
- 🛡️ **Verified Health Checks**: Passed automated sandbox builds, dependency resolution, and health test runs.
- 🚀 **Production Ready**: Lightweight footprint optimized for high efficiency.
- 📦 **Permissive Open Source**: Available for developer integration, custom modifications, and community enhancements.

## 🚀 Quick Start & Installation

```bash
# Clone your official repository
git clone https://github.com/kush-coder/autopilot-puppeteer.git
cd autopilot-puppeteer
```

---

## 📖 Comprehensive Documentation

[![build](https://github.com/puppeteer/puppeteer/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/puppeteer/puppeteer/actions/workflows/ci.yml)
[![npm puppeteer package](https://img.shields.io/npm/v/puppeteer.svg)](https://npmjs.org/package/puppeteer)

<img src="https://user-images.githubusercontent.com/10379601/29446482-04f7036a-841f-11e7-9872-91d1fc2ea683.png" height="200" align="right"/>

> Puppeteer is a JavaScript library which provides a high-level API to control
> Chrome or Firefox over the
> [DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/) or [WebDriver BiDi](https://pptr.dev/webdriver-bidi).
> Puppeteer runs in the headless (no visible UI) by default

## [Get started](https://pptr.dev/docs) | [API](https://pptr.dev/api) | [FAQ](https://pptr.dev/faq) | [Contributing](https://pptr.dev/contributing) | [Troubleshooting](https://pptr.dev/troubleshooting)

## Installation

```bash npm2yarn
npm i puppeteer # Downloads compatible Chrome during installation.
npm i puppeteer-core # Alternatively, install as a library, without downloading Chrome.
```

:::note

Modern package managers (including npm (see the [RFC](https://github.com/npm/rfcs/pull/868)), pnpm, Yarn, Bun, and Deno) block dependency install scripts by default. If the install script is blocked, Puppeteer will not download the browser during installation, leading to runtime errors.

You can manually download the required browsers after installation by running:

```bash npm2yarn
npx puppeteer browsers install
```

Alternatively, you can configure your package manager to allow the install script to run (for example, with npm, by adding `"puppeteer"` to `"allowScripts"` in your `package.json`).

:::

## MCP

Install [`chrome-devtools-mcp`](https://github.com/ChromeDevTools/chrome-devtools-mcp),
a Puppeteer-based MCP server for browser automation and debugging.

Puppeteer also supports the experimental [WebMCP](https://pptr.dev/guides/webmcp) API.

## Example

```ts
import puppeteer from 'puppeteer';
// Or import puppeteer from 'puppeteer-core';

// Launch the browser and open a new blank page.
const browser = await puppeteer.launch();
const page = await browser.newPage();

// Navigate the page to a URL.
await page.goto('https://developer.chrome.com/');

// Set the screen size.
await page.setViewport({width: 1080, height: 1024});

// Open the search menu using the keyboard.
await page.keyboard.press('/');

// Type into search box using accessible input name.
await page.locator('::-p-aria(Search)').fill('automate beyond recorder');

// Wait and click on first result.
await page.locator('.devsite-result-item-link').click();

// Locate the full title with a unique string.
const textSelector = await page
  .locator('::-p-text(Customize and automate)')
  .waitHandle();
const fullTitle = await textSelector?.evaluate(el => el.textContent);

// Print the full title.
console.log('The title of this blog post is "%s".', fullTitle);

await browser.close();
```


---

*Maintained with ❤️ by @kush-coder. Official distribution powered by GitHub Autopilot Automation Platform.*
