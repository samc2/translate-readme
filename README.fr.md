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
Nom : Traduction du fichier README

Sur :

Push :

Branches :

- main
- master
Tâches :

Build :

Système d'exploitation : ubuntu-latest

Étapes :

- Nom : Configuration de Node.js

- Utilise : actions/checkout@v5

Utilise : actions/setup-node@v6

Avec :

Version de Node : 24

- Exécuter : npm ci

- Exécuter : npm test

# Codes de langue ISO : https://cloud.google.com/translate/docs/languages

- Nom : Ajout du fichier README - Chinois simplifié

Utilise : samc2/translate-readme@main

Avec :

LANG : zh-CN

- Nom : Ajout du fichier README - Chinois traditionnel

Utilise : samc2/translate-readme@main

Avec :

LANG : zh-TW

- Nom : Ajout du fichier README - Hindi

Utilise : samc2/translate-readme@main

Avec :

LANG : hi

- Nom : Ajout README - Arabe

Utilisation : samc2/translate-readme@main

Avec :

LANG : ar

- Nom : Ajout du fichier README - Français

Utilisation : samc2/translate-readme@main

Avec :

LANG : fr

- Nom : Ajout du fichier README - Anglais

Utilisation : samc2/translate-readme@main

Avec :

LANG : en 
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
