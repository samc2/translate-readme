Traduire l’action Lisez-moi

## Traduction du fichier README

-   [Anglais](README.md)
-   [Chinois simplifié](README.zh-CN.md)
-   [Chinois traditionnel](README.zh-TW.md)
-   [hindi](README.hi.md)
-   [Française](README.fr.md)
-   [arabe](README.ar.md)
-   [English](README.en.md)

**GitHub Action pour traduire Readme dans n'importe quelle langue**

Il s'agit d'une action GitHub qui traduit automatiquement le fichier Lisez-moi de votre dépôt dans une langue spécifiée.

_Une soumission pour le[DEV : Actions GitHub pour l'Open Source !](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)hackathon_

## Installation

1.  **Ajouter un fichier de workflow**à votre projet (par ex.`.github/workflows/readme.yml`):

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

## Configuration

### Possibilités

Vous pouvez configurer davantage l'action avec les options suivantes :

-   `LANG`: La langue dans laquelle vous souhaitez traduire votre fichier Lisez-moi. La valeur par défaut est le chinois simplifié. (Je suis ghanéen) Les langues prises en charge se trouvent ci-dessous.
    (défaut:`fr`) (requis:`असत्य `)

## Langues prises en charge

Les langues prises en charge peuvent être trouvées ici<https://cloud.google.com/translate/docs/languages>

### Problèmes

Vérifier[ici](https://github.com/samc2/translate-readme/issues/1)pour les problèmes liés à cette action.

### Développement

Les suggestions et contributions sont toujours les bienvenues !

### LICENCE

[AVEC](./LICENSE)
