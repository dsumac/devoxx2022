# graphql


##

- protocole particulier
- très souvent "over http" (pas obligatoire)
  - POST tout le temps (des moyens de contournement existent) 

## modeles "archi / orga"

### monolithe devant N "api services"

### composition

- sorte de reverse proxy graphql (stitching)
  - presque tout le temps en nodeJs
- sous schémas
  - séparation des résponsabilités (sorte de bff graphql)
- passent tous par **une** gateway

#### stitching

- équipe s'occupant de la gateway: **bottleneck**
  - unique point d'entrée

- autre solution: **router**
  - chez apollo, sorte de réceptacle et d'agrégateur de schéma + outil CI


