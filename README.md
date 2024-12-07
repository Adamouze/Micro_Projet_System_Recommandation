# Contexte des métadonnées

## Schéma des données
- Taille du DataFrame metadata : 74 347 lignes
- Nombre total de musiques dans le dataset rating-only : 465 392
- Problème identifié : Seulement 74 347 musiques uniques sont disponibles, ce qui empêche de récupérer les informations pour toutes les musiques.

## Solutions
- Utilisation des liens Amazon des musiques pour compléter les données lors du filtrage collaboratif.

## Fonctions implémentées
### Get_music_info
- Récupère toutes les informations metadata d'une musique en fonction de son ID.

### Display_image
- Affiche l'image du produit à partir de l'ID de la musique.

## Outils utilisés
- Apache Spark pour la lecture et le traitement des métadonnées.

# Filtrage collaboratif (Ratings-based)
Le filtrage collaboratif basé sur les évaluations utilise les interactions entre utilisateurs pour recommander des musiques. Aucune information explicite sur la méthodologie n'a été détaillée, mais l'accent a été mis sur l'exploitation des évaluations pour des recommandations précises.

# Filtrage basé sur le contenu
## Méthodologie
Application de TF-IDF (Term Frequency-Inverse Document Frequency) pour analyser et extraire des informations pertinentes à partir des colonnes suivantes des métadonnées :
- Title
- Brand
- Category
- Description
- Feature

Cette méthode permet de recommander des musiques en se basant sur leurs descriptions et autres caractéristiques textuelles.

# Pistes d'études et mise en œuvre
## Fonctionnalités futures
- Création d'une fonction permettant de comparer les correspondances entre la liste also_buy présente dans les métadonnées et les recommandations générées. Cela améliore la précision des recommandations en prenant en compte les comportements d'achat des utilisateurs.

## Technologies utilisées
- Apache Spark pour le traitement des données massives.
- TF-IDF pour le filtrage basé sur le contenu.
- Python pour l'implémentation des fonctions de récupération et d'affichage des métadonnées.

# Exécution du projet
## Pré-requis
- Apache Spark
- Python 3.x
- Librairies : pandas, numpy, scikit-learn

## Étapes pour exécuter
1. Charger les datasets des métadonnées et des évaluations.
2. Exécuter les fonctions Get_music_info et Display_image pour enrichir les données.
3. Appliquer les méthodes de filtrage collaboratif et TF-IDF.
4. Comparer les recommandations avec la liste also_buy.

# Auteurs
- Adam OUZEGDOUH
- Pierre Laurent