#  Art et entropie - chaos eng. 


## Kintsugi

- 

## Kintsugi modern

- lego dans mur etc.
- nouveau support

## Web kintsugi

- parfaite ? non
- **resiliente**: oui

## chaos engineering

- basé sur théorie du chaos  ...
- netflix
  - aux origine du CE.
  - ils le font en prod

## avantages du CE

- meilleure compréhensio des interdépendances entre composants
- identifier **faiblesses dans un env. contrôlé**
  - Ex: serveur de geoip ne répond pas => bloque la connexion
    - pas de timeout

- confiance dans la capacité à résister dans des **conditions réalistes**
- forcer à mettre en oeuvre des systèmes de **récupération des ressources**

## pour le front

- pas grand chose aujourd'hui


## en pratique (experimental)

- etat nominal
- hypothèses
- perturbation
- comparaison

### perturbations

- http requests
  - réélles
    - lente ou qui ne répondent pas
    - ex de github
      - github avec CDN qui ne répond plus
      - continue de fonctionner sans JS et CSS
      - on peut aussi aller plus loin
        - minimum de style 'inline'
  - induites: proxifier xhr / fetch
    - ralentir manuellement les req.
- localisation
  - réélles
    - ex: bouton avec largeur qd texte change
    - calcul de ratio de char entre les langues: entre 1 et 1,19
  - induites  
   - utiliser la pseudo localisation
     - avec package npm par ex.
- timer
  - réélles
    - 1 sec = 1 sec ? oui et pourtant
    - nav ralenti le timer parfois pour des raisons de perf
  - induites: ralentir les timers avec 
- historique: sauvegarde formulaire
  - réélles
    -  ...
  - induites
    - code utilisant api native faisant back / forward dans l'historique
- clics / double clic
  - envoi d'une seule req, ex appel
- a11y
  - ajout de style permettant d'avoir le style en N&B
    - ex site devoxx: on ne fait plus la diff entre les types de conf
- viewports
  - forcer les viewports

### comment on met cela en place

- extension nav: chaos front end toolkit
  - dev par l'orateur

### survivre au chaos

- limiter le chaos à des systèmes / experimentations limitées
- pour le front: probablement pas en prod (pour l'instant ou sur des users limités)

## questions

- CI:
  - pas conseillé pas l'orateur : ritualiser en tests manuels
  - selon moi: on pourrait pour générer le test => mais plus couteux
