# REX - microfrontends

## Contexte

Rex banque suisse "Lombard Odier"
- existants app: 800 composants

- initiative modernisation "technique" et "fonctionnel"

- application G2:
  - monolithe client lourd: utilisateurs aiment le point d'entrée unique
  - multi techno: delphi, .., web etc.
  - look & feel vieillissant

## Stratégie retenue

- application web mais pas monololithe

## Composant VS microfrontend

- composant: controle fort / couplage fort
- mfe: couplage faible / contrôle faible => autonome

## Composition / découpage

- type de composition
  - verticale
  - horizontale: RETENUE

- comment ?
  - côté client RETENUE
  - côté serveur

## Comment / tech

- webpack
  - faisait déjà du lazy loading
  - maintenant, sorte de lazy loading avec module "distants"

## 

- analyse
- prototype
  - application host (shell)
  - application "widget"
- points d'attention
  - homogénéité
    - lib design commune => css

- communication entre apps
  - communication BUS
  - autres services

- approche déclarative du layout
  - cell + config => déclarative

- shell
  - uniquement responsable du routing / host générique
  - prend un fichier de config

## challenges / pitfalls

- communication service => il y a eu du partage de données entre les
  - utilisation d'un global state / pas encore beaucoup de recul sur le sujet
- widget state
  - on veut garder l'état MAIS unload / load widget => plus
  - store spécifique pour cela
- cache des requests depuis le widget
  - wrapper autour d'axios pour faire un seul appel sur un service appelé par plusieurs widget (avec un TTL)

## resultats

### avantages

- réutilisation et flexibilité
- performance: lazyloading automatique
- progressif: compatible avec l'existant, migration progressive
- centré business
  - concept techniques isolés par widget
  - ils communiquent sur "le choix métier"

### inconvénients

- gestion de l'instabilité: bcp de combinaisons de MEP etc.
- dépendances & versionning:
  - ils vont regarder unpackage
- couplage sur core-lib / design-lib
  - attentif à mettre uniquement le strict minimum
 
## aujourd'hui

- 3 apps / 15 devs / 30 pers
- developper portal (nextjs): catalogue de widget

## demain

- stratégie mobile & desktop
- gestion des permissions
- services centraux: notification, custom dashboard, widget catalog, permissions (au niveau du shell)

# plus d'info 

- Manfred Steyer, pour angular et MFF




  
