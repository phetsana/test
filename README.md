# PROFILE

## POST /session

###### Description :
Retourne les informations d'une session authentifié (profil utilisateur)

###### Code retour :
200 si login/pass OK

###### Paramètres : 
- **login** : (string) Identifiant unique utilisateur
- **pass**  : (string) Pass crypté 

###### Exemple : 

```json
{
        "_id": "4df0a81c73dbcb2350000019",
        "first_name": "Phetsana",
        "last_name" : "Phommarinh",
        "dj_name" : "",
        "email" : "test@gmail.com",
        "country": "France",
        "Bio" : "",
}
```

## POST /profile

###### Description :
Récupération et modification des infos profil

###### Code retour :
200 si OK

###### Paramètres : 
- **first_name** : (string) Prénom
- **last_name**  : (string) Nom
- **dj_name** : (string) Nom DJ
- **country** : (string) Pays
- **bio** : (string) Biographie

###### Exemple : 

```json
{
        "_id": "4df0a81c73dbcb2350000019",
        "first_name": "Phetsana",
        "last_name" : "Phommarinh",
        "dj_name" : "",
        "email" : "test@gmail.com",
        "country": "France",
        "Bio" : "",
}
```

# Songs

## GET /suggestions/{page}

###### Description :
Liste des dernières suggestions (pagination à 20 résultats, classement du plus récent au plus ancien)

###### Code retour :
200 si OK

###### Exemple : 

```json
{
        "page" : 1,
        "suggestions" : [
                {
                        "_id" : 27,
                        "artist" : "NEEDTOBREATHE",
                        "Title" : "Brother (Feat. Gavin DeGraw)",
                        "genre" : "pop",
                        "album_art" : "https://res.cloudinary.com/don2kwaju/image/upload/ar_1:1,c_fill,g_auto/w_auto:100:250/dpr_auto/f_auto,q_auto/v1460118433/covers/cqjlc0ku0o5yizn4hwgn.jpg",
                        "suggested_at" : 1436486400,
                        "suggestor" : "Arild Lekanger"
                }
        ],
}
```
