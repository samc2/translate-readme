# Readme एक्शन का अनुवाद करें

## README अनुवाद

-   [अंग्रेज़ी](README.md)
-   [सरलीकृत चीनी](README.zh-CN.md)
-   [परंपरागत चीनी](README.zh-TW.md)
-   [हिंदी](README.hi.md)
-   [फ्रेंच](README.fr.md)
-   [अरबी](README.ar.md)
-   [अंग्रेज़ी ](README.en.md)

**GitHub किसी भी भाषा में Readme का अनुवाद करने की क्रिया**

यह एक GitHub Action है जो स्वचालित रूप से आपके रेपो में निर्दिष्ट भाषा में रीडमी का अनुवाद करता है।

_के लिए एक सबमिशन[DEV: ओपन सोर्स के लिए GitHub क्रियाएँ!](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)आयोजित हैकथॉन_

## सेट अप

1.  **Add a workflow file**अपनी परियोजना के लिए (उदा।`.github/workflows/readme.yml`):


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

## विन्यास

### विकल्प

आप निम्न विकल्पों के साथ आगे की कार्रवाई को कॉन्फ़िगर कर सकते हैं:

-   `LANG`: जिस भाषा में आप अपने रीडमी का अनुवाद करना चाहते हैं। डिफ़ॉल्ट अंग्रेजी है  है।  समर्थित भाषाओं को नीचे पाया जा सकता है।
    (चूक:`en`) (आवश्यक:`false`)

## समर्थित भाषाएँ

समर्थित भाषाएं यहां पाई जा सकती हैं[हत्तपः://क्लाउड.गूगल.कॉम/ट्रांसलेट/डॉक्स/लैंग्वेजेज](https://cloud.google.com/translate/docs/languages)

### मुद्दे

जाँच[यहाँ](https://github.com/samc2/translate-readme/issues/1)इस कार्रवाई से संबंधित मुद्दों के लिए।

### विकास

सुझाव और योगदान हमेशा स्वागत है!

### लाइसेंस

[साथ में](./LICENSE)
