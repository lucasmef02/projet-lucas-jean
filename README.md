# projet-lucas-jean
Voici les différentes fonctions présentes dans le code :

afficherProduitsFaibleStock
Cette procédure affiche les produits ayant une quantité en stock inférieure ou égale à 5.
Parcourt le tableau de produits et vérifie si la quantité en stock de chaque produit est inférieure ou égale à 5.
Affiche les informations des produits correspondants.
  
afficherProduitsStockEpuise
Cette procédure affiche les produits qui sont en rupture de stock.
Parcourt le tableau de produits et vérifie si la quantité en stock de chaque produit est égale à 0.
Affiche les informations des produits correspondants.

  
afficherEspaceRestant
Cette procédure affiche l'espace utilisé dans le magasin et l'espace restant.
Calcule l'espace utilisé pour chaque taille de produit (petite, moyenne, grande) en fonction de la quantité de chaque produit.
Calcule l'espace total restant en soustrayant l'espace utilisé de la capacité maximale du magasin.
Affiche l'espace utilisé pour chaque taille de produit et l'espace total restant.

  
  
ajouterProduit
Cette procédure permet d'ajouter un produit au magasin.
Vérifie si la capacité maximale de produits est atteinte.
Crée une nouvelle instance de Produit avec les informations fournies.
Vérifie si l'espace requis pour stocker le produit est disponible.
Ajoute le produit au tableau produits et met à jour l'espace utilisé pour chaque taille de produit.
  
trouverProduitParNom
Cette fonction recherche un produit par son nom.
Parcourt le tableau de produits et compare le nom de chaque produit avec le nom recherché.
Renvoie un pointeur vers le produit s'il est trouvé, sinon renvoie NULL.

trouverProduitParReference
Cette fonction recherche un produit par son numéro de référence.
Parcourt le tableau de produits et compare le numéro de référence de chaque produit avec le numéro de référence recherché.
Renvoie un pointeur vers le produit s'il est trouvé, sinon renvoie NULL.

augmenterStock
Cette procédure permet d'augmenter le stock d'un produit.
Recherche le produit par son numéro de référence à l'aide de la fonction 

trouverProduitParReference().
Demande à l'utilisateur la quantité à ajouter.
Met à jour la quantité en stock du produit trouvé.

réduireStock
Cette fonction permet de réduire le stock d'un produit.
Recherche le produit par son numéro de référence à l'aide de la fonction 

trouverProduitParReference().
Demande à l'utilisateur la quantité à réduire.
Vérifie si la quantité demandée est disponible en stock.
Met à jour la quantité en stock du produit trouvé.


Lorsque qu’on compile le programme on a le choix entre 3 possibilités : 
 
1. Mode Gestion
2. Mode Achat
0. Quitter
 
Lorsque qu’on rentre le chiffre 1, on entre sur le mode gestion, 
 
On voit d’abord la liste d’article disponible qui ont un stock faible,
les article qui sont en rupture de stock et les articles présents dans le magasin 
 
On a le choix entre 3 possibilités : 
 
-> Mode Gestion :
1. Vérifier le stock d'un produit
2. Augmenter le stock d'un produit
0. Quitter
 
Vérifier le stock permet de d’avoir les informations sur le produit savoir son stock, sa taille et sa référence
 
Ensuite lorsque qu’on rentre 2 ont rentre sur la fonction qui permet d’augmenter le stock d’un produit, 
celui-ci permet d’augmenter le stock d’un produit dans la limite permise par le stock du magasin.
 
On peut maintenant quitter et revenir à la page principale : 
 
1. Mode Gestion
2. Mode Achat
0. Quitter
 
On peut maintenant cliquer sur 2 pour accéder au mode achat 

Dans le mode Achat on doit d'abord s'identifier, on nous demande, ainsi, notre nom et prénom 
Pour savoir si on fait partie des clients, si le client n'a pas de compte on propose de lui en créé un. 
 
Ensuite ce menu s'ouvre : 
  
-> Mode Achat
1. Acheter un produit
2. Afficher l'historique des achats
0. Quitter

En cliquant sur 1 on peut procéder à l'achat de divers produits en diverse quantités.
Le client voit ensuite apparaître le total de ses achats qui est mis dans son fichier client.
Si le client veut acheter un produit qui n'est pas en stock le programme lui propose de supprimer sa fiche client.

En appuyant sur 2 on peut consulter son historique d'achat qui nous indique l'achat passer et le numéro de référence du produit acheté.

Ensuite en cliquant sur 0 on revient au programme principal : 

1. Mode Gestion
2. Mode Achat
0. Quitter

Enfin en cliquant sur 0 on quitte le programme, il nous affiche le total dépensé et envoie un message de remerciement.


void ajouterClient
Cette procédure prend en paramètre les prénom et nom d'un client et l'ajoute au tableau clients et crée un fichier de sauvegarde pour le client.

void supprimerClient 
Cette procédure recherche dans le tableau clients, la supprime du tableau, supprime également le fichier de sauvegarde associé au client.

void effectuerAchat  
Cette procédure effectue un achat pour un client donné. Elle prend en paramètres un pointeur vers une instance de la structure Client,
un pointeur vers une instance de la structure Produit et la quantité d'achat. Elle vérifie si le produit est disponible en stock,
met à jour le stock, l'historique d'achats du client et le fichier de sauvegarde du client.
