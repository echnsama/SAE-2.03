---
title: "README"
author: "Groupe 2"
date: "28 février 2025"
---


#  **Rapport technique SAE 2.03 partie README**

**Équipe chargée du projet:**  
Enzo Dewame : enzo.dewame.etu@univ-lille.fr  
Emile Camard : emile.camard@univ-lille.fr  
Elyas Rabhiu : elyas.rabhiu@univ-lille.fr

## Présentation du projet 

Ce rapport présente le travail effectué pour mettre en place une machine virtuelle Debian sous VirtualBox. L'objectif principal était de configurer un environnement de virtualisation, d'installer un système d'exploitation de base et de gérer divers outils comme `sudo`, tout en résolvant certains défis techniques.

Nous détaillerons dans ce rapport :

- La `configuration de la machine virtuelle basique`.
- L'installation du `système d'exploitation`.
- L'importance et l'installation des suppléments invités.
- Les réponses aux questions de vocabulaire et de culture informatique.
- L'`installation automatique ` de la machine virtuelle.

Ce projet a permis de renforcer nos compétences en administration de systèmes Linux et en gestion de machines virtuelles, tout en nous confrontant à des problématiques techniques pratiques.

Pour la réalisation de ce rapport, nous avons au préalable `préparés une fiche technique au format Markdown`, incluse dans le fichier zip joint au rapport si cela vous intéresse .

**REMARQUE**  : Toute les réponses aux questions sont disponible dans un onglet du sommaire précis et sont disposés partie par partie mais les une à la suite des autres, pas comme dans le pdf semaine 1 ou elles suivent la continuité du document

### Explication:

Dans le dossier de rendu nommé `SAE 2.03` vous possédez un fichier `Rapport.md`, ce fichier nous servira de base pour ensuite obtenir la version en pdf et en html que nous vous avons mis dans le dossier.zip.

Pour les conversions nous utiliserons Pandoc pour la facilité d'utilisation, il est normalement configuré mais si vous ne l'avez pas faites: 
```bash
sudo apt install pandoc
```
Pour la version `html` il suffit de se rendre dans un terminal et de se placer dans `SAE 2.03`, cette emplacement est l'emplacement dans lequelle on `executera les commandes suivantes`:

```bash
pandoc Rapport.md --template=elegant_bootstrap_menu.html -o Rapport.html --toc --embed-resources
```
La signification :
 1) `Rapport.md` est notre fichier markdown source
 2) `--template=...` est la template html utilisé pour ajouter un style aerée a nos pages.
 3) `Rapport.html` est le format de la conversion
 4) `--toc` nous permet de faire l'automatisation de la table des matières, le sommaire.
 5) `--embed-resources` nous permet de convertir les ressources externes comme les images et les intègre dans le fichier HTML ce qui assure l'integrité des images et liens. 
 
 Pour finir ouvrez votre fichier nouvellement crée en entrant cette commande: 
 ```bash
open Rapport.html
```
Pour la version `pdf` cela a été plus compliqué, comme après plusieurs reprise nous n'arrivions pas a `génerer un fichier pdf `qui intègre la template html `avec pandoc `nous sommes passés par une autre librairie nommé `**wkhtmltopdf**`, celle ci permet de `convertir le fichier en pdf` à partir du `fichier html` nouvellement crée et `non plus du fichier markdown` 

Pour cela nous avons premièrement installé `**wkhtmltopdf**` avec la commande: 
```bash
sudo apt install wkhtmltopdf
```
Puis par la suite nous avons donc converti le html en pdf avec la commande:
```bash
wkhtmltopdf Rapport.html Rapport.pdf
```
Pour finir comme pour la conversion en html, ouvrez votre fichier pdf nouvellement crée avec la commande: 
```bash
open Rapport.pdf
```

# FIN