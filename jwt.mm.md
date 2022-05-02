# JWT

## c'est quoi un jeton ?

- jeton
  - chaine de caractères
  - jeton avec plusieurs infos

## JSON Web Token / JWT / JOT

- basé sur swt avec partie JSON en plus


## Cryptographie

- mathématiques / confiance / communication / canal non sur / non répudiation

## JWT qu'est ce que c'est 

- token.dev
- jwt.


### forme compacte

- base 64: sous forme de charge
- chaine de char
- 3 parties: entete, charge utile, signature

### sous forme JSON

- permet d'avoir plus infos: plusieurs signatures etc.

### 

- registered claims
- public claims: plus d'info (normalisé par IANA)
- private claims: ce que l'on veut

### jose

- spec
- JWT / JSON Web Signature / JSON Web Encryption / JSON Web Algo / JSON Web Key

## JWE

- JSON Web Encryption
  - 5 parties

## JWK

- - faire transiter les clefs / JSON Web Key

## cas d'usage

- OAuth2
- openIdConnect
- session stateless
  - session côté cliente
  - pas simple

## les attaques ?

- jeton non sécurisé
  - lib qui permette d'utiliser des jetons non sécurisés
- autre
- brute force
   
## conseils de secu

- ded
- na pas tout accepter
  - ne se base jamais 
- préférer l'asymétrique
  - ne pas partager de secret avec le partenaire
- utiliser des libs pour manipuler les token
- ne pas se battre pour révoquer les JWT
  - fais pour être autonome: essayer d'éviter les révocations
- ne pas se baser sur l'algo du header

## confidentialité

- c'est en clair (les infos sont en base64)
- infos nécessaires et suffisantes
- https **uniquement**

## alternatives

- biscuit
- paseto
- macarons
- branca

