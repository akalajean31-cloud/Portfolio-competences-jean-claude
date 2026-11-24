# Journal d'avancement

## Semaine 41 (6/10)
### Réalisé
- Création du dépôt GitHub
- Rédaction du README (présentation du projet)
- Réalisation du planning prévisionnel
- Maquette v1 : vue d'ensemble, compétences, projets et parcours

### Choix de conception
- Site sur une seule page avec menu latéral : le visiteur voit tout
  sans changer de page.
- Compétences en bulles : la taille montre le niveau d'un coup d'œil.
- Projets et parcours sur une même frise : on voit l'évolution dans le temps.

### Difficultés rencontrées
- Les accents ne sont pas acceptés dans le nom du dépôt.
- Les espaces dans les noms de fichiers cassent les liens Markdown.
- Première maquette trop classique : refaite avec une organisation
  plus personnelle.

### Prochaines étapes
- Lister mon vrai contenu (compétences et niveaux, projets, parcours)
- Mettre à jour la maquette avec ce contenu

## À faire
- Architecture générale du site (TD2, 23/10)
- Structure HTML/CSS
- Partie serveur (BDD + contrôleur)
- Visualisation des compétences
- Interactions (curseur, filtres, frise)
## Semaine 43
Schéma relationnel adapté à partir de l’exemple fourni : ajout des tables PROJET, NIVEAU_SEMESTRE, TECHNOLOGIE, PARCOURS et ADMIN pour correspondre aux fonctionnalités du site. 
arborescence, schéma relationnel personnalisé, adaptation au BUT SD VCOD.
## Semaine 48 (23–24/11) – TD3 : serveur et base de données

### Réalisé
- Serveur Node.js/Express connecté à PostgreSQL (Laragon)

  ![Serveur lancé](td3/preuves/serveur_lance.png)

- Script init_db.sql : tables, données, ajout de C5 et d'une image
  preuve par compétence

  ![Script SQL](td3/preuves/init_db_sql.png)

- Routes API : /api/heures, /api/competences, /api/competence/:id

  ![Route /api/heures](td3/preuves/api_heures.png)

- Récupération des données avec fetch et affichage dans la console

  ![Console](td3/preuves/console_datas.png)

- Page web : tableau, graphique en barres et camembert (Chart.js)

  ![Page avec graphiques](td3/preuves/page_graphiques.png)

- Clic sur une compétence : description et image preuve affichées

  ![Clic sur une compétence](td3/preuves/clic_competence.png)

### Difficultés rencontrées
- Virgule manquante dans le INSERT : erreur de syntaxe SQL
- ON CONFLICT DO NOTHING ne met pas à jour les lignes déjà présentes
- Compétence sans activité absente du graphique : corrigé avec LEFT JOIN
- console.log n'affiche rien sur la page : il faut ouvrir la console (F12)
  ou écrire dans le HTML

### Prochaines étapes
- Table PREUVE séparée, reliée aux apprentissages critiques
- Adapter la visualisation à mon portfolio (bulles, curseur par semestre)
