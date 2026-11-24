# Exercice 2 – Architecture : tables, serveur et routes

````mermaid
flowchart LR
  subgraph BDD["Base PostgreSQL butsd"]
    COMP["COMPETENCE<br/>(id_competence, intitule, description)"]
    ACT["ACTIVITE_PEDAGOGIQUE<br/>(num, semestre, heure, skill, id_competence)"]
    AC["APPRENTISSAGE_CRITIQUE<br/>(id_ac, intitule, niveau, id_annee, id_competence)"]
    PREUVE["PREUVE<br/>(id_preuve, image, texte, id_ac, id_etudiant)"]
  end

  SERVEUR(["API SERVER<br/>Express / Node.js"])

  COMP -- SQL --> SERVEUR
  ACT -- SQL --> SERVEUR
  AC -- SQL --> SERVEUR
  PREUVE -- SQL --> SERVEUR

  SERVEUR --> R1["/api/competences<br/>Liste complète des compétences"]
  SERVEUR --> R2["/api/heures<br/>Total heures par compétence"]
  SERVEUR --> R3["/api/competence/:id<br/>Info d'une compétence"]
  SERVEUR --> R4["/api/preuves<br/>Toutes les preuves"]
  SERVEUR --> R5["/api/preuve/:id<br/>Une preuve"]

  R1 & R2 & R3 & R4 & R5 -- "JSON (200 ou 404)" --> NAV["Navigateur<br/>index.html + Chart.js"]

  classDef nouveau fill:#ffe8a3,stroke:#b38600
  class PREUVE,AC,R4,R5 nouveau
````

En jaune : ce que j'ai ajouté au schéma du sujet.

## Explications

**Principe** : le navigateur ne lit jamais la base directement.
Il appelle une route avec `fetch` (requête HTTP GET), le serveur exécute
une requête SQL, puis renvoie le résultat en JSON.

| Route | Tables utilisées | Ce qu'elle renvoie |
|---|---|---|
| `/api/competences` | COMPETENCE (+ ACTIVITE_PEDAGOGIQUE) | la liste des compétences avec intitulé et description |
| `/api/heures` | COMPETENCE + ACTIVITE_PEDAGOGIQUE | le total des heures par compétence (`SUM` + `GROUP BY`) |
| `/api/competence/:id` | COMPETENCE | une compétence (ex : C1), 404 si elle n'existe pas |
| `/api/preuves` | PREUVE + APPRENTISSAGE_CRITIQUE | l'intégralité des preuves |
| `/api/preuve/:id` | PREUVE | une preuve précise, 404 si elle n'existe pas |

- `:id` est un **paramètre** : dans `/api/preuve/2`, `id` vaut 2.
- On lit des données, donc c'est la méthode **GET** (le R de CRUD).
````
````

## Lire le code

- `flowchart LR` : schéma de gauche à droite (LR = *left to right*). `TD` le dessine de haut en bas.
- `NOM["texte"]` : une boîte rectangulaire. `(["..."])` fait une boîte arrondie.
- `<br/>` : retour à la ligne dans une boîte.
- `A --> B` : une flèche. `A -- texte --> B` ajoute une étiquette sur la flèche.
- `subgraph ... end` : un cadre qui regroupe les tables de la base.
- `classDef` et `class` : colorient en jaune les éléments ajoutés.
- Les guillemets autour des routes sont **obligatoires** à cause du `/` et du `:`. Sans eux, Mermaid affiche une erreur.

Vérifie le rendu dans l'onglet **Preview** de l'éditeur GitHub, ou sur **mermaid.live**.

Dans ton propre code, la preuve est une colonne de COMPETENCE et non une table PREUVE. Si tu gardes cette version, retire PREUVE, R4 et R5, et ajoute `preuve` dans la boîte COMPETENCE.
