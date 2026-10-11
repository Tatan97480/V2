# BE STRONGER — Espace Coach V13.6.29

Application web autonome pour gérer des fiches clients, suivre les séances, les performances et les règlements, et utiliser les timers d’entraînement.

## Lancer l’application

Ouvrir `index.html` dans un navigateur récent. Aucune installation n’est nécessaire.

## Données et sauvegardes

Les fiches clients, échéances et règlements sont conservés dans le stockage local du navigateur (`localStorage`). Ils restent sur l’appareil et le profil de navigateur utilisés. Depuis l’onglet **Clients**, exporter régulièrement une sauvegarde JSON. La restauration remplace les données présentes.

La V13.6.29 importe les fiches existantes au premier lancement dans son propre espace de stockage afin de garder la V13.6 originale intacte. Les données restent accessibles depuis l’application et ne sont pas synchronisées entre appareils. Ne pas publier de sauvegarde JSON ni de données client dans le dépôt GitHub.

## Suivi des règlements

La vue Paiements affiche une synthèse de toutes les échéances en attente et en retard, avec le solde global par devise et un accès direct à chaque client. Avant toute restauration, l’application télécharge automatiquement une sauvegarde de sécurité. Les exports indiquent la version et la date de création.


Dans l’onglet **Paiements**, crée une échéance par client (prestation, montant, devise et date limite), enregistre les paiements totaux ou partiels, puis consulte le montant encaissé, le solde restant et les retards. Les règlements enregistrés peuvent être supprimés, ce qui recalcule le solde.

## Publier avec GitHub Pages

1. Créer un dépôt GitHub.
2. Ajouter `index.html` et `README.md` à la racine du dépôt.
3. Dans **Settings → Pages**, choisir **Deploy from a branch**, la branche `main` et le dossier `/ (root)`.
4. Enregistrer pour publier l’application.

## Timer

Le compte à rebours conserve le départ automatique après 10 secondes : bip à 3, 2 et 1, puis annonce « GO ». Le timer ajoute un bip sur chacune des 3 dernières secondes de chaque intervalle, phase ou échéance.


## Anneau du timer

L’anneau suit la progression du round courant : il se remplit à chaque intervalle EMOM et sur le round TABATA complet (effort + repos), puis repart au round suivant.


## Sens de progression de l’anneau

Le tracé du cercle progresse dans le sens inverse de la version précédente.


## Sens de progression de l’anneau

L’anneau démarre à 12 h et progresse dans le sens des aiguilles d’une montre jusqu’à compléter le round.


## Sens de progression de l’anneau

L’anneau démarre à 12 h et progresse dans le sens inverse des aiguilles d’une montre jusqu’à compléter le round.


## Annonces et bips

« HALF RIGHT THERE » est relancé proprement à la moitié de la durée. Les bips 3–2–1 marquent uniquement la fin du timer complet; les transitions de round gardent leur bip de repère.


« HALF RIGHT THERE » est annoncé à mi-round en EMOM et TABATA.


## Contraintes client

Chaque fiche client comporte un champ « Mouvements à éviter ». Saisis un ou plusieurs termes séparés par des virgules, points-virgules ou retours à la ligne. Le programme signale les exercices dont le nom contient l’un de ces termes afin que le coach les vérifie et les adapte. Les remplacements restent sous le contrôle du coach.


## Logo

Le logo BE STRONGER est intégré dans `index.html` et fonctionne hors ligne.


## Planning

L’onglet **Planning** permet de planifier, modifier et terminer les séances d’un client. Les séances terminées rejoignent son historique.

## Coordonnées et relances

Les fiches client gèrent téléphone, e-mail, début du coaching et date de relance. Le tableau de bord affiche les rendez-vous du jour, les clients dont la date de relance est atteinte et les soldes de paiement à suivre.

## Mensurations et bilans

Enregistre le poids, le tour de taille, les hanches et la poitrine au fil du temps. Le bouton **Imprimer le bilan client** crée un rapport imprimable avec le programme, l’historique et les mensurations.

## Reçus

Chaque règlement peut produire un reçu imprimable ou enregistrable en PDF depuis la fenêtre d’impression du navigateur.


## Calendrier

L’onglet Planning contient un calendrier mensuel avec repères et compte de séances. Cliquer sur une date filtre la liste des rendez-vous; « À venir » revient à la liste des prochaines séances.


Les rendez-vous du planning sont tous des coachings individuels; le type est fixé automatiquement.


## Partager un programme PDF

Dans l’onglet Programme, sélectionne un client et clique sur **Imprimer le programme en PDF**. Dans la fenêtre d’impression du navigateur, choisis **Enregistrer au format PDF**, puis transmets le fichier au client.


## Tests physiques

La rubrique Tests inclut un pacer sonore de 20 m (départ à 8,5 km/h, +0,5 km/h par palier d’une minute), une annonce vocale française du palier et de la vitesse, avec la distance cumulée annoncée au palier 5, un comptage automatique des bips-navettes (20 m par bip), le calcul en direct du kilométrage ainsi que les tests de pompes strictes (répétitions valides) et de gainage ventral (durée tenue), avec historique par client. Les bips du test utilisent une tonalité carrée synthétique à attaque franche, avec un volume renforcé pour se rapprocher du signal sonore du Luc Léger. La voix masculine dépend des voix françaises installées sur l’appareil; si aucune voix masculine n’est disponible, la synthèse utilise une voix française avec une tonalité plus grave. Le kilométrage se calcule au fil du test et la distance est annoncée au palier 5.

## Contacts et agenda iPhone

Importe des contacts depuis un fichier vCard `.vcf`. Depuis Planning, exporte les rendez-vous au format `.ics`, puis ouvre le fichier sur iPhone pour les ajouter au Calendrier. Ces échanges sont des imports/exports ponctuels; les modifications futures demandent une nouvelle exportation.

## Horloge

Le tableau de bord affiche une horloge analogique locale avec le logo BE STRONGER au centre.

## Programmes selon l’objectif

Les clients sans programme personnalisé reçoivent un modèle correspondant à leur objectif (perte de graisse, recomposition, hypertrophie, performance ou remise en forme), avec adaptation du nombre de séries pour un niveau débutant. Le bouton de réinitialisation applique le modèle et supprime les charges et validations liées à l’ancien programme.


## Horloge et mode sport

Le tableau de bord affiche le logo sur le cadran analogique, l’heure en affichage digital et un mode sport avec chronomètre démarrable, mettable en pause et réinitialisable.

## Tableau de bord

L’accueil regroupe les clients, les rendez-vous du mois et à venir, les séances du jour, les prochaines séances, les relances et les paiements à suivre.


## Navigation par menu

Les rubriques Clients, Paiements, Planning, Tests, Programme et Timer sont regroupées dans un menu hamburger à trois barres, placé à gauche du bouton Tableau de bord qui reste directement accessible. Le menu se ferme après le choix d’une rubrique, au clic extérieur ou avec la touche Échap.


La carte « Vue coach » regroupe maintenant les indicateurs et l’horloge avec le logo, son cadran digital et le chronomètre sport.


La vue coach présente les indicateurs en lignes. L’horloge est un cadran analogique noir et or avec chiffres de 1 à 12, sans logo ni mode sport.


## Progression et chronomètre de gainage

La rubrique Tests fournit un graphique d’évolution pour la distance Luc Léger, les pompes, le gainage, le poids et les mensurations. Le test de gainage comprend un chronomètre intégré; le temps mesuré remplit automatiquement le résultat à enregistrer.
\n\n## Bilan PDF d’évolution\n\nDepuis la fiche client ou le tableau de bord, ouvre « Imprimer le bilan d’évolution ». Le rapport rassemble les graphiques de progression disponibles, les résultats Luc Léger, pompes et gainage, les mensurations, le programme et l’historique récent. Dans la boîte d’impression, choisis « Enregistrer au format PDF » pour le transmettre au client.\n