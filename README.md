
# <p align="center">Tracking</p>
  
IHM de Tracking pour le suivi de production sur les sites du groupe.


## 🙇 Author
#### Yannick Levasseur
- Gitlab: [Tracking](https://gitlab.domselha.fr/python/tracking)
        

## V1.0.0
- Creation de Tracking Lot1.
## V1.1.0
- Ajout de la déconfirmation.
- Ajout de la confirmation a Zero.
- Suppression des espaces lors du Scanne OF ou du Conditionnement.
- Grisé le Bouton de validation après une réinitialisation d'un SN.
- Grisé le Bouton de conf à zero après une réinitialisation d'un SN.
- Ajout de la liste des SN qui sont terminés.
## V1.1.1
- Ajout d'une gestion d'erreur en cas de PB serveur.
## V1.1.2
- Methode timer.
- Correction de la boucle Timer , ajout d'une pause (sleep) si pas authentifier.
## V1.1.3
- Correction de l'authentification pour la fenêtre de déconfirmation.
- Nouvelle api checkdeconfirmation.
## V1.1.4
- Modification de l'identification pour prendre en compte les mots de passe.
## V1.1.5
- Modification de l'identifiant toujours en minuscule.
## V1.1.6
- Apikey vers fichier ini.
## V1.2.0
- Ajout des Fonctions de Merge, Swap et Split de conditionnement.
- Ajout du préfixe "IHM : " dans tous les messages d'erreurs venant de l'IHM.
- Fermeture de toutes les fenetres lors de la fermeture de la fenetre principale.
- Ajout d'un LOG_IHM où l'on garde les 200 dernieres lignes.
- Modification du LOG de temps ou l'on garde aussi les 200 dernieres lignes.
- Ajout des différents fond d'ecran en fonction du serveur sur lequel on travaille PROD ou RECETTE.
## V1.2.1
- Modification dans API pour l'envois des JSON.
- Modification dans suivi atelier, en cas de annuler lorsque l'on passe une carte en PASS pour la 1ere fois dans le LOT.
## V1.2.2
- Ajout d'un Check si le NewCond n'est pas sur une autre etape ou un autre OF lors d'un merge.
## V1.2.3
- API changeNumSerieStatus Ajout du champs action : normal retour reinit.
- Modification du menu clic droit pour rajout des retour en arrière et des réinit.
- Modification du change status en ajoutant le champ Action.
- Modification de la fenetre de demande de conditionnement de sortie a partir du suiviAtelier.
## V1.2.4
- Design des Fenetres     -> création de class dans le fichier design.Init_window. 
- Design des StyleSheet   -> création de class dans le fichier design.StyleSheet.
- Creation de la Fenetre A Propos.
- Creation de la Fenetre d'administration des Conditionnements.
- Ajout au Menu de la Main Window des nouvelles fenetres.
- Découpage de la class SuiviAtelier en plusieurs sous class (dans le sous répertoire suiviAtelier).
- Ajout des champs NumOpé et Opération dans la fenetre des listeConditionnements lorque l'on lance avec un OF.
## V1.3.0
- Ajout de la Gestion des OF sans SN.
- Modification de l'API changeNumSerieStatus -> barcodeIn et Out au lieu des barcodeID.
- Ajout des API changeSansNumSerieStatut, getListQtyCond, SelectConditionnementOutSansNumSerie.
- Ajout de l'accès au fichier d'Aide avec le nom du fichier en paramètre dans le fichier INI.
- Ajout de la validation lors de l'identification si une chaine est 100% Hexa (badge Selha) (on prend le risque qu'un CIL ne soit pas 100% Hexa).
- Modification du Fin de processus, nous n'envoyons plus la list des numéros de série (meme api pour le sans SN).
## V1.3.1
- Ajout de la confirmation d'opération.       
- Ajout de l'API GetListeConditionnement afin de ne plus faire appel au Launch.
- On garde les 10000 dernieres lignes des fichiers logs au lieu de 200.
- Modification de l'IHM pour préparer la descente d'information de SAP.
- Gestion d'erreur inversion du retour True<->False pour eviter les """ if "not" erreurs """.
- Correction de la déconfirmation sans SN --> non fonctionnel en 1.3.0.
- Correction de la confirmation a zero sans SN --> non fonctionnel en 1.3.0.
- Correction du enable du bouton de validation de conditionnement pour le sans SN.
- Correction du clic droit pour le sans SN.
## V1.4.0
- Ajout des champs indice SAP/ICS/Edition.
- Ajout de l'affichage des Logos (en attente des inputs).
- Ajout des champs de l'Operaion en cours (exemple date de fin d'Operation).
- Fond Vert en cas de serveur DEV.
## V1.4.1
- Creation du fichier Site.txt qui n'est pas recréé s'il existe deja.
- reincorporation des apiKey dans le fichier infos_ini.ConnectionServeur.
- Correction pour l'affichage du Nom-Prenom et de la Date Heure pour les status "a tester".
- Ajout du Login dans les retours des Api ou il faut d'identifier afin de pouvoir afficher le FullName.
- Ajout de l'Api GetCondLastEvent pour verifier les last Event.
## V1.4.2
- Correction de toutes les Api pour l'envois du SiteName en paramètre d'entrée.
## V1.4.3
- Correction d'affichage du conditionnement après le LAUNCH.
## V1.4.4
- Update last event apres une confirmation a Zero.
- Affichage du FullName via le login dans la déconfirmation, la gestion des conditionnements et l'Administration des Conditionnements.
- Renvois du Json "Complet" dans l'APi DroitTracking.is_authorised().
- Actualisation en double cliquant sur le conditionnement en cours dans le tree_view du conditionnement.
- Création des calendriers date et time pour les instructions.
- load du contenu des conditionnements dans le LoadOrderInfos sur le clic du Conditionnement cliqué.
- load du contenu des op réalisées dans les LoadSuiviAtelier sur le clic sur Réalisées.
- load du contenu des prochaines op dans les LoadSuiviAtelier sur le clic sur Prochaine étapes.
- Affichage du conditionnement en cours dans la liste des conditionnements de l'OF.
- On efface la fenetre suivi atelier si le conditionnement n'est plus rattaché à un OF.
- On deconnecte la personne en cas d'erreur lors du Launch.
- Check Version dans le Serveur.
## V1.4.5
- Correction de "Déconnection" par "Déconnexion".
- Changement du Nom de l'executable Main_Window ==> Tracking.
- Si en DEV, on ne check pas la Version avec la Base.
- Déselection automatique des lignes "Réalisées" et "Prochaines étapes" afin de ne pas les envoyers lors de d'un change Status.
- Fenetre de Conditionnement a confirmer ==> les lignes cocher sont verte et décocher blanche.
## V1.5.0
- Mise en place de l'instruction avec le champ commentaire.
- Creation du Fichier Json via l'XLS en executant Generation_FromXLS_JsonInstructions.py.
- Ajout du Site dans le titre des fenêtres.
- Ajout du Logo du Site sur la Fenetre de Suivi Atelier.
- Ajout d'infos Bulles dans le suivi Atelier.
- Empecher la validation par double clic sur la ligne pour les OF sans SN.
- Chargement des logos d'opérations en fonction des données dans le JSON.
- Affiche un logo par defaut s'il n'existe pas.
## V1.5.1
- Ajout de la commande "self.setAttribute(QtCore.Qt.WA_DeleteOnClose)" dans le Init de toutes les Fenetres afin de libérer l'espace mémoire après le Close de celle-ci.
- Correction lorsqu'on ferme la fenetre d'instruction avec la Croix, seule la fenetre d'instruction se ferme.
## V1.5.2
- Modification de ExitWindowlogged pour supprimer les variables des fenetres fermées
## V1.5.3
- Le calendrier dans les instructions apparait plus ou moins grand en fonction de la résolution de l'ecran            
## V1.5.4
- Bloquage des instruction pour les Sans SN car cela ne fonctionne pas ==> bouton Disable ! 
- Logos operation 70*70
- Affichage des instrucitons sur 2 colonnes et lieu de lignes par lignes
## V1.5.5
- Laisser la posssibilité de valider le conditionnement meme si tout les champs d'instructions ne sont pas remplit.
## V1.5.6
- Afficher les logos en 100x100 --> modification de la taille des logos en 100x100
- Modification du fond des calendriers
- Disable le bouton des instructions s'il n'y en a pas mais on affiche quand meme le logo s'il y en a un    
## V1.5.7
- Ajout du CheckLastEvent au click sur le bouton instruction.     
## V1.5.8
- Ajout d'un skip pour les instructions Visa.
## V1.5.9
- Correction pour les instructions Visa venant du JSON (evite le decalage).
- Ajout de la possibilité d'avoir des chiffres numérique avec des "." en plus de "," dans les champs numérique des instructions
## V1.6.0
- Modification de l'appel, sans le load .UI, de toutes les fenetres
- Ajout du Check de la version du Json et retéléchargement en cas de PB.
- Ajout du Telechargement du fichier Json d'instruction en TFTP si la version est mauvaise ou que le fichier est corrompu.
- Modification de l'API pour les checks versions (Version Tracking + JSON).
- Gestion des conditionnements : Verification en amont si le conditionnement de sortie existe.
- Téléchargement des Logos opération en TFTP s'il n'existe pas sur le poste.
- Téléchargement des Logos d'OF (article) en TFTP s'il n'existe pas sur le poste.
- Mise a jour automatique de Tracking lorsqu'on est pas sur TSE.
- Affiche le Conditionnement en cours en Vert dans la liste des conditionnement de l'OF. (ne charge plus les SN ou Qté sur simple clic).
- Ajout de la Désignation d'article.
- Ajout de la prise en compte des Logos d'entête.
- Retourne une Erreur en cas de probleme dans les types de reponses du fichier JSON.
- Prise en compte des types d'instruction issu du fichier Excel (TextLibre,TextNumerique,TextMultilignes).
- Possibilité d'imprimer les informations de l'OF par clic Droit dans le TreeViewOF avec codes barre.
- Catch du message d'erreur -1 ==> Confirmation PostConso.
- Envoi du site dans toutes les API.
- Ajout du VISA dans les instructions.
- Ajout du Numero de Lot de l'OF depuis l'API GetCond (dans la partie OF et dans l'impression du Document OF).
- Ajout du Poste de Travail.
- Modification du message d'erreur en cas d'OF pas connu sur un autre site que celui sélectionné.
- Modification des fiches d'OF (contenu et Font de l'OF).
- Ajout du Check si Tracking est deja ouvert sur la session en cours. 
## V1.6.1
- Ajout des DLL. 
## V1.6.2
- Mise à jour par patch si pas de patch sur le TFTP ==> mise à jour par MSI.
- Ne prends pas en compte la ligne "Prochaine Etapes" lors d'une multiselection pour le change numero de série status.
- Ajout de l'API Fin de Processus sans SN (séparation des avec et sans SN).
- Repertoire d'installation différent selon le Type de Tracking "PROD" ou autre.
- Encodage / Decodage en UTF-8 au lieu de ASCII pour les mots de passe dans les API.
- Ajout de l'edition / ICS dans l'impression, si ce n'est pas Vide dans SAP.
## V1.6.3
- Tue le process de Tracking lorsque le message "Tracking est déja ouvert sur cette session" apparait.
## V1.6.4
- Correction pour le telechargement TFTP des logos d'entete car il ajouté .jpg a chaque fois.
## V1.6.5
- Mofification des Feuilles d'impression d'OF.
- Ajout d'un popup pour informer l'opérateur de la fin de process, L'OF est terminé.
## V1.6.6
- Eviter les plantages lors de la création de code barre si le champs est vide.
- Correction controle de Version Tracking et Json.
- Correction du bug lors du Scan SN pour changer le Status.
## V1.6.7
- Correction du popup pour informer l'opérateur de la fin de process et/ou que L'OF est terminé.   
## V1.6.8
- Correction du ELIF eu lieu du IF pour la reucpération du serveur TFTP pour EINEA.
- Correction du d'un I majusucle par un i minucule ligne 294 (gridLayout_instructions) dans instruction.py.
- Correction de rataché par rattaché dans Conditionnement.py ligne 387.
## V1.7.0
- Gestion de Lots.
- Ajout du copier dans les clics droits sur les Zones TreeWidgets.
- Ajout setToolTip sur les Logos.
- Correction si l'on ferme la fenetre d'identification par la X, si le champs est vide on met le flag Annuler a True.
## V1.7.1
- Modification des conditions de l'affichage des infos INDICE SAP - ICS - EDITION - EDITION_Prod.
- Ajout de la proposition de rÃ©imprimmer la feuille de conditionnement si les cartes du condionnement est partiellement validé.
## V1.7.2
- Si Virtuel, on ne demande pas a réimprimer la feuille du Conditionnement IN. 
## V1.8.0
- Ajout du Skip.
- Ajout dans le suiviAtelier du Numéro de Lot dans l'affichage.
- Remplacement des "A Tester" par "A Faire".
- Remplacement des "Pass" par "Fait".
- Ajout du Clic droit, valider les numéros de série par Numéro de Lot.
- Gestion du Conditionnement REBUT.
- Ajout d'un fichier de constantes ==> contient toutes les variables communes.
- Nouvelle Gestions des messages d'erreurs a partir du fichier de Const.
- Ajout des Bip lors du scann des numéros de séries. (bon ou mauvais)
## V1.8.1
- Ajout de l'affichage de l'instruction si c'est le 1er change status.
- Ajout de la possibilité de valider un conditionnement avec des cartes "A Faire" et "Fait" pour skiper certaine carte du conditionnement
- Ajout d'un Popup de confirmation de monté en Stock des SN ou des produits lors de la fin de Processus.
- Ajout d'un Popup lorsque le Numero de série scanné n'est pas dans la liste.
## V1.8.2
- Correction sur le popup de fin de flux partiel de l'OF (erreur de position d'une parenthèse).
- Correction du Check de l'instruction sur l'enssemble des conditions dans la fonction : CheckValidButtonEnabled.
- Ajout de Décorateur sur chaque grande class afin de garder dans le log IHM les crachs possible.
## V1.8.3
- Gestion du codeRfcMiseEnStock pour savoir si c'est un message d'information ou d'erreur.
- Correction pour le disable du bonton de confirmation à Zero.
- Modification @dresses serveur SELHA : from alfrescoprd.domselha.fr to selha_app01.domselha.fr.
- Ajout des quantités réalisées/confirmées (confirmées - (skip+rebut)).
- Correction s'il ne reste que 2 conditionnements rebut et terminé sur l'OF.
## V1.8.4
- Affichage en rouge du message de fin en cas d'erreur.
- Ajout du nombre de skip dans le survole dans le suivi-atelier.
## V1.8.5
- Ajout de la feuille d'impression de Mise en Stock.
- Mise en place de la fermeture de tracking pour maintenance.
## V1.8.6
- Blocage du Bug sur la date de fermeture de tracking pour maintenance.
## V1.8.7
- Correction Bug pour la date de fermeture de tracking pour maintenance.
## V1.9.0
- Ajout des Fenetres REBUT et RETOUR EN PROD.
- Ajout du Clic droit de mise en Attente.
- Ajout de la gestion des installations via patch ou MSI selon une version minimum pour les patchs en base.
- On disable la fenetre de suivi et le champ scanne SN si c'est pas un conditionnement Production.
- Ajout de la feuille d'impression de Mise en Stock pour alerte qualité.
- Encodage du fichier Site.txt sous un autre répertoire (dans le fichier de const).
- Insertion du code d'activation (qui correspond au site) dans le fichier ini.
## V1.9.1
- Modification pour garder le fichier Site.txt pour les TSE.
- Prise en compte du Init_Site_Code dans GmotParam.
- Modification de la Variable Globale ServeurVersion par gmotParam.
- Correction si on met en Etuve sur un Cond Virtuel, on affecte bien le temps au bon Cond Virtuel que l'on a recu en retour.
## V1.9.2
- Modification pour garder le fichier Site.txt pour les TSE.
- Ajout du Check du Jour pour les horraires de fermeture de la maintenance.
- Séparation de la montée en Stock dans la fin de Flux et dans la mise en attente s'il y a un magasin.
- Ajout du popup pour saisir le text de 25 charactère max lors de la montée en stock.
- Ajout du message de mise ne stock dans le document de sortie marchandise.
## V1.9.3
- Correction de la variable JsonResponseMiseEnStock["login"] (sans le self) dans le ChangeStateSuiviAtelier.
- Correction du paramètre 'Skipped' dans la fonction checkSkip.
- Ajout du Check du CondWait avant de faire la mise en stock pour les AQ.
- Modification du Skip Opération ==> on ne fais plus l'instruction depuis l'IHM, c'est fait coté Serveur en Base.
## V1.9.3.1
- Correction sur la compatibilité d'un conditionnement Virtuel Free (obligatoirement compatible) : if CondWait == "CondVirtuel" lors du changeStatus.
## V1.9.3.2
- Modification des change status Wait pour mettre l'impression de la Sortie marchandise apres la MAJ Tracking en cas de magasin.
- Modification du getInfosConditionnementCompatible avec ajout du fonctionIdCible car le condIn est obligatoirement de Prod.
## V1.9.3.3
- Correction du message en Json du SkipOpe.
## V1.9.3.4	
- Correction d'une Gestion d'Erreur en cas PB d'accès au serveur.
- Ajout du Check du CondOut avant de faire le Merge des conditionnements.
## V1.9.4
- Ajout du Champ Text de l'OF venant de SAP + l'api : getTextSapOrder.
- Ajout du Champ Text de l'OF venant de SAP sur la feuille d'impression du conditionnement.
- Désactivation de la gestion de l'impression Recto-Verso, c'est l'imprimante qui gère.
- Modification des Log_IHM pour que ce soit plus explicite.
- Modification pour le Skip Opération d'un conditionnement : Ajout des infos OF / Num OP / Designation OP / Poste de Travail.
- Ajout d'un message de "NON" mise en stock en cas d'annulation lors de la demande du message et s'il est obligatoire (cas de Lots).
- Ajout des Fonctions dans la liste des conditionnements dans l'appel via l'OF.
- Ajout des Fonctions des conditionnements dans la Fenêtre de Déconfirmation.
## V1.9.4.1
- Modification du Logo sur le message popup d'evolution du fichier d'instruction.
- Modification siu le fichier encrypté existe, il est prioritaire et on ecrase le code activation dans le fichier Ini.
- Modification de la police et de la couleur du text d'OF.
## V1.9.4.2
- Fichier encrypté du site pour la recette/dev est différent du tracking Prod.
- Modification de la police et de la couleur du text d'OF en pourpre.
- Impression du Text d'impression, ajout des retours chariots + diminution de la taille de police.
- Blocage avc Init de la fenetre suiviAtelier s'il y a une erreur de SAP sur la clé "ZTXT".
