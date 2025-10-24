# 翻譯自述動作

## 自述翻譯

-   [英語](README.md)
-   [簡體中文](README.zh-CN.md)
-   [繁體中文](README.zh-TW.md)
-   [印地語](README.hi.md)
-   [法文](README.fr.md)
-   [阿拉伯](README.ar.md)
-   [English](README.en.md)

**GitHub Action將自述文件翻譯成任何語言**

這是一個GitHub Action，可自動將您回購中的自述文件翻譯成指定的語言。

_提交的[DEV：開源的GitHub行動！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客馬拉松_

## 設定

1.  **添加工作流程文件**到您的項目中（例如`.github/workflows/readme.yml`):


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
          # ISO Langusge Codes: https://cloud.google.com/translate/docs/languages  
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
          - name: Adding README - English
            uses: samc2/translate-readme@main
            with:
              LANG: en

## 組態

### 選件

您可以使用以下選項進一步配置操作：

-   `LANG`：您要將自述文件翻譯成的語言。預設為英語。 可以在下面找到支持的語言。
    （默認：`en`）（必填：`false`)

## 支持的語言

支持的語言可以在這裡找到<https://cloud.google.com/translate/docs/languages>

### 問題

檢查一下[這裡](https://github.com/samc2/translate-readme/issues/1)有關與此操作有關的問題。

### 發展歷程

隨時歡迎提出建議和貢獻！

### 執照

[與](./LICENSE)
