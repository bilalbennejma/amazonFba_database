# amazonFba_database

L’objectif de cette base de données est de modéliser une marketplace de type Amazon FBA, mettant en relation des vendeurs et des clients via une plateforme.

Elle doit permettre de gérer l’ensemble du processus de vente :
de la mise en ligne d’un produit jusqu’à sa livraison au client.

La base de données doit permettre entre autre de :

- Enregistrer les vendeurs et leurs informations.
- Enregistrer les produits et les associer aux vendeurs.
- Gérer les stocks et connaître les quantités disponibles.
- Enregistrer les clients et leurs adresses.
- Créer et suivre les commandes (statut : en attente, payée, expédiée, livrée, annulée).
- Enregistrer les paiements associés aux commandes.
- Suivre les livraisons (transporteur, numéro de suivi).
- Gérer les retours et remboursements.
- Permettre l’analyse des ventes (chiffre d’affaires, produits les plus vendus, vendeurs les plus performants).

En résumé, cette base doit permettre de suivre les stocks, les commandes et les transactions financières, tout en assurant une gestion complète de l’activité commerciale de la plateforme.

Table PRODUITS : id_prod, nom_produit, description, prix_unitaire, stock, nom_vendeur, email_vendeur (Ici, l'email du vendeur est redondant avec le nom).
Table COMMANDES : id_comm, date_commande, id_client, nom_client, adresse_client, telephone_client, montant_total (Ici, les infos clients sont stockées directement dans la commande : c'est la redondance parfaite pour le projet ).
Table DETAIL_COMMANDE : id_comm, id_prod, quantite, nom_produit_copie (On recopie le nom du produit, encore une redondance).
