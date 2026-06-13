# DustEthic - implémentation de référence

Code de référence du standard DustEthic : transformer des dusts crypto en dons vérifiables pour des ONG, par agrégation par actif, avec consentement explicite et sans garde opaque.

## Statut

**Phase 0 - aucun code recommandé en production.**

Ce dépôt est destiné à accueillir un prototype et une implémentation de référence. À ce jour :

- aucun contrat DustEthic n'est audité ;
- aucun déploiement mainnet n'est recommandé ;
- aucune collecte de fonds n'est réalisée par DustEthic ;
- aucun token DustEthic n'existe ;
- toute expérimentation doit rester testnet ou simulation tant que le standard, l'audit et la validation juridique ne sont pas terminés.

## Documentation officielle

La spécification vit dans le dépôt documentation : <https://github.com/DustEthic/docs>

Documents à lire avant de coder :

- Standard : <https://github.com/DustEthic/docs/blob/main/STANDARD.md>
- Veille technique : <https://github.com/DustEthic/docs/blob/main/TECHNICAL-WATCH.md>
- Feuille de route : <https://github.com/DustEthic/docs/blob/main/ROADMAP.md>
- Sécurité : <https://github.com/DustEthic/docs/blob/main/SECURITY.md>

## Principe technique

Le modèle cible doit permettre :

1. détection ou choix d'un dust ;
2. consentement explicite de l'utilisateur ;
3. autorisation limitée ou intention signée ;
4. agrégation par actif ;
5. exécution seulement si le lot est viable ;
6. réception ONG ;
7. preuve publique lisible et vérifiable.

## Contraintes de conception

- L'utilisateur conserve ses clés.
- Les permissions doivent être ciblées, limitées et révocables quand le modèle le permet.
- Le relayeur ne doit pas être une boîte noire.
- Les frais doivent être visibles avant et après exécution.
- Une transaction ou une intention ne doit jamais être présentée comme un don exécuté sans preuve.
- Toute implémentation touchant à des fonds doit être auditée avant usage réel.

## Pistes à étudier

- x402 / HTTP 402 pour exprimer des micro-paiements ou intentions.
- ERC-4337 pour smart accounts, UserOperations, bundlers et paymasters.
- EIP-7702 pour batching ou sponsoring côté EOA, avec vigilance forte sur les délégations.
- EIP-5792 pour appels groupés côté wallets.
- ERC-7683 pour intents cross-chain, encore à traiter comme brouillon.
- CCTP pour certains flux USDC, sans en faire une dépendance unique.

Ces pistes ne sont pas des intégrations validées.

## Feuille de route code

1. Simulateur de lots sans fonds réels.
2. Schéma JSON d'intention.
3. Schéma JSON de preuve.
4. Prototype testnet.
5. Tests automatisés.
6. Revue sécurité.
7. Revue juridique.
8. Pilote limité uniquement si les étapes précédentes sont concluantes.

## Contribuer

Les issues et pull requests sont bienvenues, mais toute proposition doit préciser le problème, l'hypothèse, les risques et les sources.

Discord : <https://discord.gg/fVFc26GV>

## Licence

Code sous licence MIT, voir `LICENSE`.

## Avertissement

Selon la juridiction et l'architecture retenue, un opérateur d'agrégation peut relever de règles applicables aux paiements, dons, actifs numériques, fiscalité ou intermédiaires financiers. Ce dépôt ne fournit pas de conseil juridique.