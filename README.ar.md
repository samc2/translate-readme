# ترجمة الإجراء التمهيدي

## اقرأني الترجمة

-   [إنجليزي](README.md)
-   [الصينية المبسطة](README.zh-CN.md)
-   [الصينية التقليدية](README.zh-TW.md)
-   [الهندية](README.hi.md)
-   [فرنسي](README.fr.md)
-   [عربى](README.ar.md)

**إجراء GitHub لترجمة الملف التمهيدي إلى أي لغة**

هذا هو إجراء GitHub الذي يقوم تلقائيًا بترجمة الملف التمهيدي في الريبو الخاص بك إلى لغة محددة.

_تقديم ل[DEV: إجراءات GitHub للمصدر المفتوح!](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)hackathon_

## يثبت

1.  **إضافة ملف سير العمل**لمشروعك (على سبيل المثال`.github/workflows/readme.yml`):

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
      - uses: actions/checkout@v2
      - name: Setup Node.js
        uses: actions/setup-node@v1
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
          LANG: en
- name: Adding README - English
        uses: samc2/translate-readme@main
        with:
          LANG: en
```

## إعدادات

### خيارات

يمكنك تكوين الإجراء بشكل أكبر باستخدام الخيارات التالية:

-   `LANG`: اللغة التي تريد ترجمة الملف التمهيدي إليها. الافتراضي هو الصينية المبسطة. (أنا غاني) يمكن العثور على اللغات المدعومة أدناه.
    (تقصير:`zh-CH`) (مطلوب:`false`)

## اللغات المدعومة

اللغات المدعومة يمكن العثور عليها هنا<https://cloud.google.com/translate/docs/languages>

### مشاكل

يفحص[هنا](https://github.com/samc2/translate-readme/issues/1)للقضايا المتعلقة بهذا الإجراء.

### تطوير

الاقتراحات والمساهمات هي موضع ترحيب دائما!

### رخصة

[مع](./LICENSE)
