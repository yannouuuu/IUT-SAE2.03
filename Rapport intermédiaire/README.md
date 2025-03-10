# Procédures pour obtenir notre rapport

## En HTML

Executez la commande suivant dans le répertoire du projet :

```bash
pandoc RapportSAE.md -o RapportSAE.html --standalone --css=RapportSAE.css --self-contained
```

> **ATTENTION**  
> Le css et l'html doivent être dans le même dossier, sinon il faudra indiquer le chemin dans la commande

## En PDF

Executez la commande suivant dans le répertoire du projet :

```bash
pandoc RapportSAE.md -o RapportSAE.pdf --pdf-engine=xelatex -V
```

## Notes sur le rendu/Todo

- [ ] Mettre les images dans un répertoire dédié
- [ ] Refaire le style de l'export PDF (demande beaucoup trop de patience)
