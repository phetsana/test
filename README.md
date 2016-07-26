# API

###### POST /session

**Description** : Retourne les informations d'une session authentifié (profil utilisateur)
**Code retour** : 200 si login/pass OK
**Paramètres** : 
- *login* : Identifiant unique utilisateur
- *pass*  : Pass crypté 

```json
{
        "_id": "4df0a81c73dbcb2350000019",
        "device": {
            "type": "android",
            "uid": "d424dfe566130b94c4318e8c4fd33cdb"
        },
        "location_type": "auto",
        "location": {
            "latitude":2.43263808,
            "longitude":48.72016451
        },
        "pseudo": "hug",
        "gender": "m",
        "birthdate": "1976-12-13",
        "age": 39
}
```
