<br/>
<p align="center">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://github.com/yannouuuu/IUT-SAE1.01/raw/main/.github/assets/header_univlille_light.png" width="200px">
        <img alt="UnivLilleLogo" src="https://github.com/yannouuuu/IUT-SAE1.01/raw/main/.github/assets/header_univlille_dark.png" width="200px">
    </picture>
  <h1 align="center">IUT-SAE2.03 | Installation de
services réseaux</h1>
</p>

<p align="center">
    Module de gestion de services réseaux 
    <br/>
    Markdown - Pandoc - Gitea - Debian
    <br/>
    <br/>
    <a href="https://moodle.univ-lille.fr/course/view.php?id=30827&sectionid=266881"><strong>Voir la page sur le moodle »</strong></a>
    <br/>
    <br/>
    <a href="https://github.com/yannouuuu/IUT-SAE2.03/"><strong>Voir le projet complet sur GitHub »</strong></a>
</p>

<br/>

## Procédures pour obtenir notre rapport

> **ATTENTION**  
> Le css et l'html doivent être dans le même dossier, sinon il faudra indiquer le chemin dans la commande

### En HTML

Executez la commande suivant dans la racine du projet :

```bash
pandoc RapportSAE.md -o output/RapportSAE.html --include-before-body=./cover/cover.html --css=./css/style.css --standalone --toc
```

-   `-o [...]` <br>
    Spécifie le fichier de sortie (abréviation de --output), c’est-à-dire le nom du fichier généré par Pandoc.
-   `--include-before-body=[...]` <br>
    Indique d’insérer le contenu d’un fichier HTML spécifique juste avant le corps (`<body>`) du document généré.
-   `--css=[...]` <br>
    Indique d’inclure un fichier CSS pour styliser le document HTML généré.
-   `--standalone` <br>
    Indique de générer un document HTML complet, avec toutes les balises nécessaires (`<html>`, `<head>`, `<body>`, etc.), plutôt qu’un fragment HTML.
-   `--toc` <br>
    Demande de générer automatiquement une table des matières (sommaire) basée sur les titres du document Markdown.

### En PDF

Executez la commande suivant dans la racine du projet :

```bash
pandoc RapportSAE.md -o output/RapportSAE.pdf --pdf-engine=weasyprint --include-before-body=./cover/cover.html --css=./css/style.css --toc
```

-   `--pdf-engine=[...]` <br>
    Indique quel moteur utiliser pour générer le PDF (WeasyPrint, Xelatex, ...)

## Structure du rapport

```plaintext
IUT-SAE2.03/
├── README.md                     # Instructions et présentation du projet
├── RapportSAE.md                 # Contenu principal du rapport
├── cover/
│   └── cover.html                # Page de couverture pour le rapport
├── css/
│   └── style.css                 # Styles pour le rapport généré
├── output/
│   └── RapportSAE.html           # Rapport généré en HTML
│   └── RapportSAE.pdf            # Rapport généré en PDF
├── shots/                        # Dossier contenant les captures d'écran
│   ├── debra.png
│   ├── gitea1.png
│   ├── gitea2.png
│   └── ...
└── test/
    └── RapportSAE.css            # Fichier CSS alternatif de tests effectués en amont
```

## To-Do List

-   [x] Mettre les images dans un répertoire dédié
-   [x] Refaire le style de l'export PDF (demande beaucoup trop de patience)
-   [x] Mettre les auteurs dans le README
-   [x] Migrer vers Weasyprint plutot que Xelatex (pour un meilleur support de la prise en charge d'édition pdf à l'aide d'un fichier css)

---

### Remerciements

Nous tenons à créditer **JEAN CARLE, SANTANA MAIA Deise et tous autre enseignant(-chercheur)** pour la création des diaporamas de cours, des TP, TD et pour la réalisation des SAE. Leur travail a été précieux pour notre apprentissage.

<br/>
<p align="center">
    <picture>
        <img alt="UnivLilleLogo" src="https://github.com/yannouuuu/IUT-SAE1.01/raw/main/.github/assets/footer_univlille.png">
    </picture>
</p>
