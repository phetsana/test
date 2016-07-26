# API

## POST /session

###### Description :
Retourne les informations d'une session authentifié (profil utilisateur)

###### Code retour :
200 si login/pass OK

###### Paramètres : 
- **login** : Identifiant unique utilisateur
- **pass**  : Pass crypté 

```json
{
        "_id": "4df0a81c73dbcb2350000019",
        "first_name": "Phetsana",
        "last_name" : "Phommarinh",
        "dj_name" : "";
        "email" : "test@gmail.com",
        "country": "France",
        "Bio" : ""
}
```
