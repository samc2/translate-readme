# 翻譯自述動作

## 自述翻譯

-   [英語](README.md)
-   [簡體中文](README.zh-CN.md)
-   [繁體中文](README.zh-TW.md)
-   [印地語](README.hi.md)
-   [法文](README.fr.md)
-   [阿拉伯](README.ar.md)
-   [英語](README.en.md)

**GitHub Action將自述文件翻譯成任何語言**

這是一個GitHub Action，可自動將您回購中的自述文件翻譯成指定的語言。

_提交的[DEV：開源的GitHub行動！](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)黑客馬拉松_

## 設定

1.  **添加工作流程文件**到您的項目中（例如`.github/workflows/readme.yml`):


    名稱： 翻譯自述文件

於：
  推：
    分支機構：
      - 主要
      - 大師
職位：
  構建：
    運行：烏班圖-最新版
    步驟：
     -  名稱：安裝 Node.js
        使用：行動/結帳@v5
        使用：操作/設置節點@v6
        與：
          節點版本：24
      - 運行：新項目管理 詞
      - 運行：新項目管理 測試
      # 國際標準化組織 語言代碼：https://cloud.google.com/translate/docs/languages  
     - 名稱：添加 添加自述文件 - 繁體中文
        使用：samc2/translate-readme@main
        與：
          蘭格: zh-CN
     - 名稱：添加 添加自述文件 - 繁體中文
        使用：samc2/translate-readme@main
        與：
          蘭格: zh-TW
     - 名稱：添加自述文件 - 印地語
        使用：samc2/translate-readme@main
        與：
          蘭格：hi
     - 名稱：添加自述文件 - 阿拉伯語
        使用：samc2/translate-readme@main
        與：
          蘭格：ar
     - 名稱：添加自述文件 - 法語
        使用：samc2/translate-readme@main
        與：
          蘭格: fr
     - 名稱：添加自述文件 - 英文
        使用：samc2/translate-readme@main
        與：
          語言: en

## 組態

### 選件

您可以使用以下選項進一步配置操作：

-   `只是`：您要將自述文件翻譯成的語言。預設為英語。 可以在下面找到支持的語言。
    （默認：`在`）（必填：`錯誤的`)

## 支持的語言

支持的語言可以在這裡找到<https://cloud.google.com/translate/docs/languages>

### 問題

檢查一下[這裡](https://github.com/samc2/translate-readme/issues/1)有關與此操作有關的問題。

### 發展歷程

隨時歡迎提出建議和貢獻！

### 執照

[與](./LICENSE)
