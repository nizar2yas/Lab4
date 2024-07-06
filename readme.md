# Lab Mise en Pratique des Tables Incrémentales dans Dataform
### Objectif du Lab
Ce lab a pour objectif de démontrer la mise en pratique des tables incrémentales dans Dataform. nous allons modifié la table `stg_transactions` pour la rendre incrémentale, ce qui permettra d'optimiser le traitement des données en ne traitant que les nouvelles données ajoutées depuis la dernière exécution.
### Contexte
Nous disposons actulement de la table stg_transactions qui contient des enregistrements de transactions de ventes. Cette table est actuellement mise à jour en traitant l'ensemble des données historiques à chaque exécution. Pour améliorer l'efficacité, nous allons transformer cette table pour qu'elle ne traite que les nouvelles transactions depuis la dernière mise à jour.

### Étapes du Lab
1. **Connexion à Dataform et Création du Projet**
   * Connectez-vous à votre compte Dataform.
   * reprenez le lab3
2. **Création d'une Table Incrémentale**
   * modifier la table stg_transactions pour devenir une table incremental.