[![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)](https://jupyter.org/)

# Quels candidats ont gagné de justesse en 2024 ?

## Contexte

Ce mini-projet a pour unique but de répondre à la question suivante : qui sont les candidats aux élections législatives de 2024 qui ont remporté leur siège avec la plus petite marge d'avance sur le second candidat ?

Considérant la nature du projet, le code a été réalisé dans une optique "one-shot" : sans stocker les données intermédiaires, sans visualisation poussée, uniquement pour répondre à la question posée.

## Méthodologie 

1. Scrapping des résultats des élections législatives 2024 sur le site du Ministère de l'Intérieur, via la bibliothèque `requests` et `BeautifulSoup`.

2. Agrégation des résultats dans un DataFrame `pandas`.

3. Calcul de l'avance absolue (en nombre de voix) et relative (en pourcentage des voix exprimées) entre le candidat arrivé en tête et le second.

4. Tri des résultats pour identifier les 3 candidats ayant remporté leur siège avec la plus petite marge d'avance absolue.

## Résultat 

🥇 Nous pouvons applaudir le maire de la 3e circonscription d'Ardèche, M. Fabrice BRUN, qui a remporté son siège avec seulement 35 voix de plus que le seconde candidat, sur un total de 58 918 voix exprimées. Cela représente une avance relative de seulement 0,06% des voix exprimées :

| # | Candidat             | Nuance | Voix  | % Inscrits | % Exprimés | Élu(e) |
|---|----------------------|--------|-------|------------|-------------|--------|
| 0 | M. Fabrice BRUN      | DVD    | 20414 | 25.20      | 34.65       | OUI    |
| 1 | M. Cyrille GRANGIER  | RN     | 20379 | 25.16      | 34.59       | NON    |
| 2 | Mme Florence PALLOT  | UG     | 18125 | 22.37      | 30.76       | NON    |

🥈 En deuxième position, la 5ème circonscription de Côte-d'Or : 
- Avance absolue : 44 voix
- Avance relative : 0.08 % des voix exprimées

| # | Candidat              | Nuance | Voix  | % Inscrits | % Exprimés | Élu(e) |
|---|-----------------------|--------|-------|------------|-------------|--------|
| 0 | M. René LIORET        | RN     | 28677 | 33.51      | 50.04       | OUI    |
| 1 | M. Didier PARIS       | ENS    | 28633 | 33.46      | 49.96       | NON    |

🥉 Enfin, en troisième position sur notre podium, la 3ème circonscription de Charente-Maritime :
- Avance absolue : 63 voix
- Avance relative : 0.12 % des voix exprimées

| # | Candidat              | Nuance | Voix  | % Inscrits | % Exprimés | Élu(e) |
|---|-----------------------|--------|-------|------------|-------------|--------|
| 0 | M. Fabrice BARUSSEAU  | UG     | 26441 | 31.58      | 50.06       | OUI    |
| 1 | M. Stéphane MORIN     | RN     | 26378 | 31.50      | 49.94       | NON    |


## Remarques

Projet réalisé le 08/07/2024. La structure du site du gouvernement ayant évolué depuis la réalisation de ce projet, le code nécessiterait quelques ajustements pour fonctionner à nouveau.