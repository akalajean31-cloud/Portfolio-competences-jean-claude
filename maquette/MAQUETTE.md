# Maquette du site – version 1

## Choix d'organisation
Site sur une seule page qui défile, avec un menu latéral fixe.
Raison : le visiteur (recruteur) parcourt tout sans changer de page,
et le menu montre à quel endroit il se trouve.

## Vue d'ensemble
```
+------+--------------------------------------------+
|  JC  |                                            |
|      |   SECTION 1 : PRÉSENTATION                 |
|  ●   |   Gros titre : « Jean-Claude »             |
|  ○   |   Une phrase qui me résume                 |
|  ○   |   [Télécharger mon CV]                     |
|  ○   |                                            |
|      +--------------------------------------------+
| MENU |   SECTION 2 : COMPÉTENCES                  |
| FIXE |   (voir détail plus bas)                   |
|      +--------------------------------------------+
|      |   SECTION 3 : PROJETS ET PARCOURS          |
|      |   (frise horizontale)                      |
|      +--------------------------------------------+
|      |   SECTION 4 : CONTACT                      |
+------+--------------------------------------------+
● = section en cours, ○ = autres sections (cliquables)
```

## Section Compétences
```
+---------------------------------------------------+
|  Semestre : S1 ---●--- S2 ----- S3 ----- S4       |
|                  (curseur)                        |
|                                                   |
|        (  HTML  )      ( SQL )                    |
|     ( Travail      (     JavaScript    )          |
|       d'équipe )          ( Git )                 |
|                                                   |
|  Taille de la bulle = niveau                      |
|  Couleur = technique / humaine                    |
|  Survol : nom + niveau | Clic : surligne les      |
|  projets liés dans la frise                       |
+---------------------------------------------------+
```

## Section Projets et parcours
```
+---------------------------------------------------+
|  <  2024 ------- 2025 ------- 2026  >             |
|      |            |            |                  |
|    [Bac]     [Projet 1]   [Projet 2]              |
|              [Entrée IUT]  [Stage]                |
|                                                   |
|  Clic sur un élément : panneau de détail          |
|  (description, technos, lien GitHub)              |
+---------------------------------------------------+
```

## Section Contact
```
+---------------------------------------------------+
|  Une ligne : email | GitHub | LinkedIn            |
+---------------------------------------------------+
```

## Interactions prévues
- Menu latéral : clic = défilement vers la section
- Curseur de semestre : les bulles grossissent selon ma progression
- Survol d'une bulle : info-bulle avec le niveau
- Clic sur une bulle : surbrillance des projets liés (vues liées)
- Clic sur un élément de la frise : panneau de détail

## Évolutions de la maquette
- v1 : première version
