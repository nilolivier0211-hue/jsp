---
name: compact
description: Quand l'utilisateur écrit "COMPACT", résume toute la conversation en 5-7 points clés (contexte critique, décisions, snippets de code) dans un format à copier-coller dans un nouveau chat.
---

# COMPACT

Déclencheur : l'utilisateur dit « COMPACT ».

## Consignes

Résume toute la conversation en **5 à 7 points clés**, en français (sauf si l'utilisateur a travaillé dans une autre langue).

Chaque point doit couvrir, selon le cas :
- le contexte critique (objectif, contraintes, état actuel du projet)
- les décisions prises et leur raison
- les fichiers, chemins, commandes et noms importants
- les snippets de code essentiels, copiés tels quels dans des blocs de code
- les points ouverts et les prochaines étapes

N'invente rien : ne mentionne que ce qui a réellement été dit ou fait. Omets les échanges sans valeur (politesses, essais abandonnés), sauf si l'échec explique une décision.

## Format de sortie

Produis un seul bloc de texte autonome, utilisable tel quel dans un nouveau chat :

````
# Contexte de la conversation précédente

1. **<Titre court>** — <détail>
2. **<Titre court>** — <détail>
   ```<langage>
   <snippet si nécessaire>
   ```
...

**Prochaine étape :** <ce qu'il reste à faire>
````

Mets l'ensemble dans un bloc de code Markdown pour faciliter la copie. N'ajoute aucun commentaire avant ou après.
