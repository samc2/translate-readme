# Translate Readme Action

## README Translation
- [English](README.en.md)
- [简体中文](README.zh-CN.md)
- [繁体中文](README.zh-TW.md)
- [हिंदी](README.hi.md)
- [Française](README.fr.md)
- [عربى](README.ar.md)

**GitHub Action to translate Readme to any language**

This is a GitHub Action that automatically translate the readme in your repo to a specified language.

_A submission for the [DEV: GitHub Actions For Open Source!](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn) hackathon_

## Setup

1. **Add a workflow file** to your project (e.g. `.github/workflows/readme.yml`):


name: Translate README

on:
  push:
    branches:
      - main
      - master
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Setup Node.js
      - uses: actions/checkout@v5
        uses: actions/setup-node@v6
        with:
          node-version: 24
      - run: npm ci
      - run: npm test
      # ISO Language Codes: https://cloud.google.com/translate/docs/languages
     - name: Adding README - English
        uses: samc2/translate-readme@main
        with:
          LANG: en  
      - name: Adding README - Chinese Simplified
        uses: samc2/translate-readme@main
        with:
          LANG: zh-CN
      - name: Adding README - Chinese Traditional
        uses: samc2/translate-readme@main
        with:
          LANG: zh-TW
      - name: Adding README - Hindi
        uses: samc2/translate-readme@main
        with:
          LANG: hi
      - name: Adding README - Arabic
        uses: samc2/translate-readme@main
        with:
          LANG: ar
      - name: Adding README - French
        uses: samc2/translate-readme@main
        with:
          LANG: fr

## Configuration

### Options

You can configure the action further with the following options:

- `LANG`: The language you want to translate your readme to. The default is English. The supported languages can be found below.
  (default: `en`) (required: `false`)

## Supported Languages

Languages supported can be found here https://cloud.google.com/translate/docs/languages

### Issues

Check [here](https://github.com/samc2/translate-readme/issues/1) for issues related to this action.

### Development

Suggestions and contributions are always welcome!

### LICENSE

[MIT](./LICENSE)
