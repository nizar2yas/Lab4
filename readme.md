<<<<<<< HEAD
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
=======
# Lab Mise en Pratique des Tables Incrémentales dans Dataform
### Objectif du Lab
Ce lab a pour objectif de démontrer la mise en pratique des tables incrémentales dans Dataform. Nous allons construire une nouvelle table incrémentale `fct_transactions` à partir de la table `stg_transactions`, ce qui permettra d'optimiser le traitement des données en ne traitant que les nouvelles données ajoutées depuis la dernière exécution.

### Contexte
Nous disposons actuellement de la table `stg_transactions` qui contient des enregistrements de transactions de ventes. Cette table est alimentée en continu par les transactions générées par la source. Pour faire de l'analytics, nous avons besoin d'une table qui contienne les données les plus fraîches. Pour améliorer l'efficacité, cette table ne traitera que les nouvelles transactions depuis la dernière mise à jour.

### Étapes du Lab
1. **Connexion à Dataform et Création du Projet**
   * Connectez-vous à votre compte Dataform.
   * reprenez le lab3
2. **Création d'une Table Incrémentale**
   * Créez une nouvelle table `fct_transactions` en utilisant la table source `stg_transactions`.
   * Configurez la table pour qu'elle soit incrémentale.
   * Utilisez `transaction_id` comme clé unique.
   * Filtrez les données pour ne prendre que les transactions de la veille.
>>>>>>> refs/heads/main
