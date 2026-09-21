# Zymo — démonstration

Démonstration publique de **Zymo**, un logiciel de gestion pour brasseries :
comptabilité matière, traçabilité de lots, droits d'accise, DRM et facturation
électronique.

**→ https://stefanialex.github.io/zymo-demo/**

## Ce que contient ce dépôt

Uniquement le **build compilé** de la démonstration, et le workflow qui le
publie. Le code source est développé dans un dépôt privé.

## Les calculs sont réels

Les accises, la DRM, les coûts de revient et la validation Factur-X affichés à
l'écran sont **calculés**, pas maquettés. Le moteur métier n'a aucune
dépendance d'exécution, il tourne donc tel quel dans le navigateur.

Ce qui est calculé, notamment :

- **Droits d'accise bière** sur le barème 2026 (arrêté du 30 décembre 2025) :
  4,12 €/hL/°Plato pour une petite brasserie indépendante, assis sur le degré
  Plato et non sur le volume seul.
- **DRM** mensuelle, avec détection d'anomalies bloquantes.
- **Factur-X / EN 16931** : règles BR et BR-CO vérifiées sur la facture
  produite.
- **Affectation FEFO** des lots et valorisation au coût moyen pondéré.

## Les données sont inventées

Brasserie, communes, clients, lots et volumes sont **synthétiques**. Aucune
donnée d'une brasserie réelle n'apparaît ici, et un test de bout en bout
échoue si un nom réel est réintroduit par mégarde.

Le jeu de démonstration contient **une anomalie volontaire** — un lot vendu
au-delà du volume produit — pour montrer ce que le logiciel fait d'un cas
dégradé plutôt qu'un scénario parfait : le solde passe en négatif et la DRM du
mois est bloquée tant qu'il n'est pas corrigé.
