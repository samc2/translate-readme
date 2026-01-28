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

    नाम: रीडमी  का अनुवाद करें
चालू:
पुश:
शाखाएँ:
- मुख्य
  मास्टर
  कार्य:
  बिल्ड:
  रन-ऑन: ubuntu-latest
  चरण:
- नाम: Node.js
  सेटअप करें उपयोग: क्रियाएँ/चेकआउट @v5
उपयोग: actions/setup-node@v6
साथ:
नोड संस्करण: 24
- चलाएँ: NPM सीआई 
- चलाएँ: NPM परीक्षा 
# ISO भाषा कोड: https://cloud.google.com/translate/docs/languages
- नाम: रीडमी  जोड़ना - सरलीकृत चीनी
उपयोग: samc2/translate-readme@main
साथ:
भाषा: zh-CN
- नाम: रीडमी  जोड़ना - पारंपरिक चीनी
उपयोग: samc2/translate-readme@main
साथ:
भाषा: zh-TW
- नाम: रीडमी  जोड़ना - हिंदी
उपयोग: samc2/translate-readme@main
साथ:
भाषा: hi
नाम: रीडमी  जोड़ना - अरबी
उपयोग: samc2/translate-readme@main
साथ:
भाषा: अरबी
- नाम: रीडमी  जोड़ना - फ्रेंच
उपयोग: samc2/translate-readme@main
साथ:
भाषा: फ्रेंच
- नाम: रीडमी  जोड़ना - अंग्रेज़ी
उपयोग: samc2/translate-readme@main
साथ:
भाषा: अंग्रेजी   

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
