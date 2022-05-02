# Chaos engineering / litmus & jenkins

## micro front end

- plusieurs solutions pour faire des micros front end
- livre "building micro frontend" O'Reilly

- ici on parle de la solution "module federation"


## webpack

- script bundler

- routing de niveau 2 => routing dans application "micro frontend"


## points d'attention

- la gestion du routing 1er/2eme niveau est un point d'attention
  -  a gérer avec webpack / a tuner 
- point d'attention sur intégration des multiples frameworks / libs
  - les libs de haut niveau: react / vue / angular etc.
    - le versionning => risque de compatibilité
  - les libs partagées ou nécessaires depuis l'application "shell"
    - axios pour le fetching (depuis appli shell angular par ex)

- communication entre les modules
  - /!\ Ne pas coupler un micro service avec un autre

- creuser la notion de SSR dans ce cas la
