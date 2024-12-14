# Analyse en Composantes Principales Parcimonieuse (SPCA)

Ce dépôt implémente les algorithmes décrits dans l’article *"Sparse Principal Component Analysis"* de Hui Zou et al. Ces méthodes visent à améliorer l’Analyse en Composantes Principales (ACP) en introduisant de la parcimonie, rendant les résultats plus interprétables tout en conservant les propriétés fondamentales de réduction de la variance de l’ACP classique. Ce travail a été réalisé dans le cadre d’un projet universitaire pour la matière *Apprentissage Non Supervisé*.

---

## Présentation

L’**Analyse en Composantes Principales** (ACP) est une méthode bien connue pour réduire la dimensionnalité des données et extraire des caractéristiques. Cependant, les composantes principales produites par l’ACP classique sont des combinaisons linéaires de **toutes les variables**, ce qui rend leur interprétation difficile.

L’**Analyse en Composantes Principales Parcimonieuse** (SPCA) résout ce problème en imposant une contrainte de parcimonie sur les composantes principales. Cela permet  d’améliorer l’interprétation des composantes en réduisant le nombre de variables contributives.

Les algorithmes SPCA s’appuient sur la régularisation Elastic Net, qui combine des pénalités \( l_1 \) (lasso) et \( l_2 \) (ridge) pour obtenir un équilibre entre parcimonie et stabilité.

---

## Contenu du dépôt

Le dépôt contient les implémentations des deux algorithmes de SPCA présentés dans l'article, adaptés à différents types de données :  

1. **Cas \( N > P \)** : Lorsque le nombre d'individus (\( N \)) est supérieur au nombre de variables (\( P \)).  
   - Fichier : `algo_N>P.R`
   - Exemple : Analyse classique de données multidimensionnelles.

2. **Cas \( P > N \)** : Lorsque le nombre de variables (\( P \)) est supérieur au nombre d'individus (\( N \)).  
   - Fichier : `SPCA_P>N.R`
   - Exemple : Analyse de données génomiques (ex. : étude de gènes).

Dans chaque fichier :
- L’algorithme SPCA est implémenté manuellement.
- Une comparaison est effectuée avec l'algorithme de la bibliothèque **R elasticnet**, qui correspond à l’implémentation officielle décrite dans l’article.

---
