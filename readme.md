# Introduction
Dans ce lab, nous avons appliqué ce que nous avons appris sur la création de tables et les différents paramètres que nous pouvons y appliquer. L'objectif du lab est de :
* **Création des tables de staging**: Créer des tables de staging en se basant sur les tables sources créées lors du lab précédent.
* **Préparation des données**: Formater et nettoyer les données des tables sources.
* **Optimisation des tables de staging**: Optimiser les données en définissant le clustering et le partitioning, ainsi que la définition des tags et labels.

### Création des tables de staging
Pour chaque table source créée lors du lab précédent, créer une table de staging. Par exemple, pour products, créer `stg_products`.
### Préparation des données
1. **Formatage des types de colonnes**: Dans le lab précédent, toutes les colonnes étaient de type *STRING*. Il est donc nécessaire de les reformater pour attribuer les bons types.
2. **Renommage des colonnes**: Renommer certaines colonnes, par exemple, au lieu de `updated_at` ou `created_at`, il est préférable de mettre `update_date` ou `creation_date`.
3. **Nettoyage des données**: Les données reçues contiennent parfois des valeurs absurdes ou incorrectes (par exemple des valeurs nulles). Éliminer ces valeurs.
### Optimisation des tables de staging
1. **Partitioning et clustering**: Afin de réduire les coûts de stockage et de requêtage, partitionner et clusteriser les tables de staging créées.
2. **Tags et labels** : Pour faciliter l'identification et la manipulation, définir des tags et labels. Par exemple, utiliser le tag `staging`.
