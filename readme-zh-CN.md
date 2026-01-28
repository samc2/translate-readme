# 翻译自述动作

## 自述翻译

-   [英语](README.md)
-   [简体中文](README.zh-CN.md)
-   [繁体中文](README.zh-TW.md)
-   [印地语](README.hi.md)
-   [法文](README.fr.md)
-   [阿拉伯](README.ar.md)
-   [英语](README.en.md)

**GitHub Action将自述文件翻译成任何语言**

这是一个GitHub Action，可自动将您回购中的自述文件翻译成指定的语言。

_提交的[DEV：开源的GitHub行动！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客马拉松_

## 设定

1.  **添加工作流程文件**到您的项目中（例如`.github/workflows/readme.yml`):

              名称：翻译自述文件

于：
  推：
    分支机构：
      - 主要
      - 大师
职位：
  构建：
    运行：乌班图-最新的
    步骤：
     - 使用：行动/结帐@v2
     - 名称：安装 Node.js
        使用：操作/设置节点@v1
        与：
          节点版本：24
      - 运行：新项目管理 词
      - 运行：新项目管理 测试
      # 国际标准化组织 语言代码：https://cloud.google.com/translate/docs/languages  
     - 名称：添加 自述文件 - 简体中文
        使用：samc2/translate-readme@main
        与：
          兰格: zh-CN
     - 名称：添加 自述文件 - 繁体中文
        使用：samc2/translate-readme@main
        与：
          兰格: zh-TW
     - 名称：添加 自述文件 - 印地语
        使用：samc2/translate-readme@main
        与：
          兰格：hi
     - 名称：添加 自述文件 - 阿拉伯语
        使用：samc2/translate-readme@main
        与：
          兰格：ar
     - 名称：添加 自述文件 - 法语
        使用：samc2/translate-readme@main
        与：
          兰格: fr
     - 名称：添加 自述文件 - 英文
        使用：samc2/translate-readme@main
        与：
          语言: en
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
