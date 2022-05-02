# CI/CD, le divorce est-il prononcé

## historique

### CI

- rappel sur les étapes (d'abord build etc.)

### CD

- plusieurs def
  - delivery
    - mettre un livrable à dispo
  - deployement
    - ...
  - development
    - rendre le dev en prod directement

## CI + CD

- rencontre des 2: pipeline
  - dessin
  - des gens autours

### démarche

- définir obj. et contraintes
- définir étapes
  - eventstorming
- définir feedbacks à remonter
- choisir des outils
- implémenter les pipelines
  - commencer petit
  - dessiner pipeline

### élément perturbateur

- everything as code
  - tous dans le code
- peu devenir compliqué / illisible

### comment aider ?

- thérapie de couple => CI & CD
- DRY
  - factoriser du code mais .... pas trop loin
- SOLID
  - S single resp. décpoupage: ex un job de deploy qui fait plusieurs composants => faire un job par composant
  - O : 
  - L : rien
  - I (interface segregation): découpage
  - D (dependency inversion): on ne veut pas découper contrat, ex: job qui fait le deploy ne se préoccupe pas du build avant mais du fait que l'artefact est lisible / accessible

### feedback

- devops est bien le rapprochement de CI & CD
- accompagnateurs
- question de comm.

### le point / les possibilités

- séparation CI / CD
  - CI construction / assemblage
  - CD mise en service / règles  
  - peut-être une étape
- une équipe de médiation devops
- intégration culture devops
  - plus compliqué

