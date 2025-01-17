# Lab Mise en Pratique des Tables Incrémentales dans Dataform
### Objectif du Lab
Ce lab a pour objectif de démontrer la mise en pratique des tables incrémentales dans Dataform. Nous allons construire une nouvelle table incrémentale `fct_transactions` à partir de la table `stg_transactions`, ce qui permettra d'optimiser le traitement des données en ne traitant que les nouvelles données ajoutées depuis la dernière exécution.
nous allons aussi créer les tables dim, qui vont servire comme dimentions à utiliser par la suite.

### Contexte
Nous disposons actuellement des tables `stg_transactions` qui contient des enregistrements de transactions de ventes. Cette table est alimentée en continu par les transactions générées par la source. Pour faire de l'analytics, nous avons besoin d'une table qui contienne les données les plus fraîches. Pour améliorer l'efficacité, cette table ne traitera que les nouvelles transactions depuis la dernière mise à jour.

### Étapes du Lab
1. **Connexion à Dataform et Création du Projet**
   * Connectez-vous à votre compte Dataform.
   * reprenez le lab3
2. **Création d'une Table Incrémentale**
   * Créez une nouvelle table `fct_transactions` en utilisant la table source `stg_transactions`.
   * Configurez la table pour qu'elle soit incrémentale.
   * Utilisez `transaction_id` comme clé unique.
   * Filtrez les données pour ne prendre que les transactions de la veille.
3. **Création des tables dim**
   * Créé les tables `dim_`, Ces tables doivent être créées en utilisant les données les plus récentes disponibles dans les tables `stg_`. Assurez-vous que les données sont correctement dédupliquées et nettoyées pour refléter l'état actuel et précis des produits et des clients.
