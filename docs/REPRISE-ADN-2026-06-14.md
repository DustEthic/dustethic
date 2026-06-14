# Reprise ADN DustEthic - gel du code

Date : 2026-06-14
Dépôt : `DustEthic/dustethic`
Statut : dépôt code / prototype, gelé pendant le réalignement du standard.

## Décision

Le prototype wallet et le code applicatif ne doivent pas être relancés tant que le standard DustEthic Phase 0 n'est pas réaligné, relu et validé dans `DustEthic/docs`.

Ce dépôt est donc placé en gel fonctionnel :

- pas de reprise du prototype wallet ;
- pas de nouvelle logique produit ;
- pas de promesse utilisateur ;
- pas de token ;
- pas de collecte par DustEthic ;
- pas de raisonnement prioritaire en fiat ;
- pas de modification destructive.

## ADN à préserver avant toute reprise du code

Toute future reprise technique devra respecter l'ADN historique DustEthic :

- DustEthic est d'abord un standard ouvert Phase 0, pas un produit financier prêt à vendre ;
- les montants doivent être raisonnés en unités crypto, pas en valeur fiat fluctuante ;
- politique `L2-first` ;
- gas policy v0.2 ;
- exécution seulement si le ratio `montant agrégé / gas estimé >= T` est suffisant ;
- repère historique : `T >= 30` ;
- plafond public historique de commission : 15 % ;
- preuve de lot publique ;
- rôles séparés : donateur, wallet, relayeur, ONG.

## Rôle de ce dépôt

Ce dépôt ne doit pas définir l'ADN du projet.

La source de vérité du standard doit être le dépôt `DustEthic/docs`.
Le dépôt historique `s-informatique/dustethic` sert de référence de migration et de mémoire.
Ce dépôt `DustEthic/dustethic` ne doit reprendre vie qu'après validation du standard.

## Prochaine étape autorisée

Avant tout travail de code :

1. finaliser la PR de réalignement dans `DustEthic/docs` ;
2. vérifier que le standard couvre l'ADN historique ;
3. seulement ensuite décider si un prototype technique vaut encore la peine.
