
# Exercice 1 – Schéma relationnel

```mermaid
erDiagram
  COMPETENCE ||--o{ ACTIVITE_PEDAGOGIQUE : "id_competence"
  COMPETENCE ||--o{ APPRENTISSAGE_CRITIQUE : "id_competence"
  ANNEE ||--o{ APPRENTISSAGE_CRITIQUE : "id_annee"
  APPRENTISSAGE_CRITIQUE ||--o{ PREUVE : "id_ac"
  ETUDIANT ||--o{ PREUVE : "id_etudiant"

  COMPETENCE {
    char id_competence PK
    text intitule
    text description
  }
  ACTIVITE_PEDAGOGIQUE {
    int num PK
    int semestre
    int heure
    text skill
    char id_competence FK
  }
  ANNEE {
    char id_annee PK
    text intitule
  }
  APPRENTISSAGE_CRITIQUE {
    varchar id_ac PK
    text intitule
    int niveau
    char id_annee FK
    char id_competence FK
  }
  ETUDIANT {
    int id_etudiant PK
    text nom
    text prenom
  }
  PREUVE {
    int id_preuve PK
    text image "nom du fichier, ex : preuve1.png"
    text texte
    varchar id_ac FK
    int id_etudiant FK
  }
```

## Explications
- Dans le schéma de départ, il y avait deux groupes séparés :
  COMPETENCE–ACTIVITE_PEDAGOGIQUE et ANNEE–APPRENTISSAGE_CRITIQUE.
- J'ai ajouté `id_competence` dans APPRENTISSAGE_CRITIQUE, car chaque AC
  appartient à une compétence. Maintenant toutes les tables sont reliées.
- J'ai ajouté ETUDIANT et PREUVE : une preuve (image et/ou texte) montre
  qu'un étudiant a acquis un apprentissage critique.
