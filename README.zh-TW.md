# 翻譯自述文件操作

## 自述文件翻譯

-   [英語](README.md)
-   [簡體中文](README.zh-CN.md)
-   [繁體中文](README.zh-TW.md)
-   [印地語](README.hi.md)
-   [法語](README.fr.md)
-   [English](README.en.md)
-   [عربى](README.ar.md)

**GitHub Action 將自述文件翻譯成任何語言**

這是一個 GitHub Action，可自動將存儲庫中的自述文件翻譯為指定語言。

_提交給[DEV：開源的 GitHub 行動！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客松_

## 設定

1.  **添加工作流程文件**到您的項目（例如`.github/workflows/readme.yml`):

```yaml
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
```

## 配置

### 選項

您可以使用以下選項進一步配置操作：

-   `LANG`：您要將自述文件翻譯成的語言。預設為英語。 支持的語言可以在下面找到。
    (預設:`en`） （必需的：`false`)

## 支持的語言

可以在此處找到支持的語言<https://cloud.google.com/translate/docs/languages>

### 問題

查看[這裡](https://github.com/samc2/translate-readme/issues/1)對於與此操作相關的問題。

### 發展

隨時歡迎提出建議和貢獻！

### 執照

[和](./LICENSE)
