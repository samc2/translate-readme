# 翻译自述文件操作

## 自述文件翻译

-   [英语](README.md)
-   [简体中文](README.zh-CN.md)
-   [繁体中文](README.zh-TW.md)
-   [印地语](README.hi.md)
-   [法语](README.fr.md)
-   [阿拉伯](README.ar.md)
-   [English](README.en.md)

**GitHub Action 将自述文件翻译成任何语言**

This is a GitHub Action that automatically translate the readme in your repo to a specified language.

_提交给[DEV：开源的 GitHub 行动！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客马拉松_

## 设置

1.  **添加工作流程文件**到您的项目（例如`.github/workflows/readme.yml`):

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

### 选项

您可以使用以下选项进一步配置操作：

-   `LANG`: The language you want to translate your readme to. The default is English. The supported languages can be found below.
    (default: `en`） （必需的：`false`)

## 支持的语言

可以在此处找到支持的语言<https://cloud.google.com/translate/docs/languages>

### 问题

查看[这里](https://github.com/samc2/translate-readme/issues/1)对于与此操作相关的问题。

### 发展

随时欢迎提出建议和贡献！

### 执照

[和](./LICENSE)
