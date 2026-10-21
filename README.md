# Portfolio de compétences – Jean-Claude

Site web présentant mes compétences (acquises à l'IUT ou en dehors),
projet réalisé dans le cadre de l'IUT.

## 1. Analyse des besoins

### Objectif
Mettre en valeur mes compétences, mes projets et mon parcours de façon
claire et visuelle, pour donner envie de me recruter ou de m'accepter
en formation.

### Public visé
- **Recruteurs** (stage, alternance, emploi) : veulent voir rapidement
  mes compétences, mon niveau et des projets concrets.
- **Écoles d'ingénieurs** (jury d'admission) : veulent comprendre mon
  parcours, ma progression et ma motivation.

### Besoins identifiés
- Voir mes compétences et mon niveau en un coup d'œil.
- Constater ma progression au fil des semestres.
- Accéder au détail de mes projets (technologies, lien GitHub).
- Télécharger mon CV et me contacter facilement.
- Pour moi : pouvoir mettre à jour le contenu sans modifier le code.

## 2. Fonctionnalités

### Navigation
- Site sur une seule page avec un menu latéral fixe.
- Clic dans le menu : défilement jusqu'à la section choisie.
- Le menu indique la section en cours de lecture.

### Visualisation
- Compétences affichées en bulles (taille = niveau).
- Curseur par semestre pour voir ma progression.
- Clic sur une bulle : mise en évidence des projets liés.
- Frise chronologique des projets et du parcours, avec panneau de détail.

### Connexion (espace administrateur)
- Page de connexion réservée à l'administrateur (moi).
- Une fois connecté : ajouter, modifier ou supprimer des compétences,
  des projets et des étapes du parcours.
- Les données sont enregistrées dans une base de données.
- Déconnexion et retour au site.

## 3. Organisation du contenu

### Arborescence du site
```
index
├── index#presentation   → nom, présentation, CV
├── index#competences    → bulles de compétences (données de la BDD)
├── index#projets        → frise projets et parcours (données de la BDD)
├── index#contact        → email, GitHub, LinkedIn
└── connexion            → formulaire de connexion
    └── administration   → gestion des données (BDD)
        └── déconnexion  → retour à index
```

### Données utilisées
Informations personnelles saisies par moi-même et stockées dans une base
de données : compétences (nom, catégorie, niveau par semestre), projets
(titre, description, technologies, date, lien) et parcours (dates, étapes).

## Technologies
À compléter au cours du projet (HTML, CSS, JavaScript, base de données…).

## Lancer le projet
À compléter lorsque le site sera développé.

## Organisation du dépôt
- `README.md` : présentation du projet
- `PLANNING.md` : planning prévisionnel et suivi
- `AVANCEMENT.md` : journal de bord semaine par semaine
- `maquette/` : maquettes du site

## Difficultés et limitations connues
À compléter au fil du projet.
