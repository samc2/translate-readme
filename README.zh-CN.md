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
名称：翻译 自述文件 
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
    -  名称：安装 Node.js
        使用：行动/结帐@v5
        使用：操作/设置节点@v6
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
