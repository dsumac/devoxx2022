#  Doctolib 

## architecture

- boring architecture
  - archi **simple** by design

- approche pragmatique

- ruby on rails

## evolution

- simple BDs Heroku
- bare metal chez hebergeur => raisons légales
- cloud aws 
  - aurora: postgresql avec couche "shared storage" spécifique aws
    - distribuée

## why aurora

- 100% postgresql 
- auto scaling
- low replication => simplifie le développement
- multi region
 

## PG expertise on App side

- code spécifique dans l'app sur le moteur

## tests de charge

- approche pragmatique: est-ce qu'il est temps de ne rien faire
  - tests avec traffic * 2 => si OK on ne fait rien

## au moment du "covid"

- tests de charge => ne permettait de voir les problèmes
  - car cas d'usage 'prise de rendez-vous' pas dans les cas de test
- base aurora *déjà au max*

## les options pour la suite 

- plan A: swith to a bigger database
- plan B: split database 

## database plus grosse

- postgresql ou 99% compatible
- * 10 à long terme (pas * 2)

## methodologie

- shortlist
  - pick candidates: spanner, yugabyte, citrus MX, vites
- même étapes de tests tous les candidats

## solutions étudiées

### Spanner

- cons
  - lot of simple **rewrites => 50%**
  - uniquement chez google

### citus MX

- need to rewrite lot of code
- limitation TODO...

### yugabyte

- pas d'autoscaling
- assez cher


## finalement

- postgresql => peu aller très loin (très performant)
...

## la suite

- plan A: toujours en étude
- plan B: split the database
  - continue la dessus
  - ...
