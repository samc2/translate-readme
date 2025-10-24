# 翻译自述动作

## 自述翻译

-   [英语](README.md)
-   [简体中文](README.zh-CN.md)
-   [繁体中文](README.zh-TW.md)
-   [印地语](README.hi.md)
-   [法文](README.fr.md)
-   [阿拉伯](README.ar.md)
-   [English](README.en.md)

**GitHub Action将自述文件翻译成任何语言**

这是一个GitHub Action，可自动将您回购中的自述文件翻译成指定的语言。

_提交的[DEV：开源的GitHub行动！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客马拉松_

## 设定

1.  **添加工作流程文件**到您的项目中（例如`.github/workflows/readme.yml`):


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

## 组态

### 选件

您可以使用以下选项进一步配置操作：

-   `LANG`：您要将自述文件翻译成的语言。默认为英语 。 可以在下面找到支持的语言。
    （默认：`en`）（必填：`false`)

## 支持的语言

支持的语言可以在这里找到[HTTPS://cloud.Google.com/translate/docs/languages](https://cloud.google.com/translate/docs/languages)

### 问题

检查一下[这里](https://github.com/samc2/translate-readme/issues/1)有关与此操作有关的问题。

### 发展历程

随时欢迎提出建议和贡献！

### 执照

[与](./LICENSE)
