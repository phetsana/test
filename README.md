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

# MUSIC

## GET /suggestions/{page}

###### Description :
Liste des dernières suggestions (pagination à 20 résultats, classement du plus récent au plus ancien)

###### Code retour :
200 si OK

###### Paramètres : 
- **page** : (GET) Numéro page

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

## GET /top10/{month}

###### Description :
Liste du top10 

###### Code retour :
200 si OK

###### Paramètres : 
- **month** : (GET) mois {1-12}

###### Exemple : 

```json
{
        "status" : "{voting|voted|published}",
        "date" : "01-06-2016",
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

## POST /top10/{month}

###### Description :
Vote pour le top10 d'un mois

###### Code retour :
200 si OK

###### Paramètres : 
- **month** : (GET) mois {1-12}
- **top10** : (array) tableau d'id de song

###### Exemple : 

```json
{
        "status_return" : "{0|1}",
}
```

# WEST COAST SWING

## GET /happenings/{page}

###### Description :
Liste des events à venir

###### Code retour :
200 si OK

###### Paramètres : 
- **page** : (GET) page

###### Exemple : 

```json
{
        "name" : "Dimanche West Coast Swing Au StudioDiabolo",
        "description" : "Dimanche aux platines DJ GBL\r\nSalle Climatisée et une Grosse VMC\r\nun endroit très convivial dans un cadre des années Fifties",
        "start_ts" : 1460309400,
        "end_ts" : 1460323800,
        "cover_path" : "https://res.cloudinary.com/don2kwaju/image/upload/ar_16:9,c_fill,g_custom/w_auto:100:250/dpr_auto/f_auto,q_auto/v1/wsdjs/missing_avatar.jpg",
        "type" : "{party}",
        "venue" : {
                "id" : 6,
                "name" : "StudioDiabolo",
                "latitude" : 48.813253,
                "longitude" : 2.360869,
        }
}
```

## GET /venues/{latitude}/{longitude}

###### Description :
Liste des events à venir sur une carte

###### Code retour :
200 si OK

###### Paramètres : 
- **latitude** : (GET) latitude
- **longitude** : (GET) longitude

###### Exemple : 

```json
{
        "name" : "Dimanche West Coast Swing Au StudioDiabolo",
        "description" : "Dimanche aux platines DJ GBL\r\nSalle Climatisée et une Grosse VMC\r\nun endroit très convivial dans un cadre des années Fifties",
        "start_ts" : 1460309400,
        "end_ts" : 1460323800,
        "cover_path" : "https://res.cloudinary.com/don2kwaju/image/upload/ar_16:9,c_fill,g_custom/w_auto:100:250/dpr_auto/f_auto,q_auto/v1/wsdjs/missing_avatar.jpg",
        "type" : "{party}",
        "venue" : {
                "id" : 6,
                "name" : "StudioDiabolo",
                "latitude" : 48.813253,
                "longitude" : 2.360869,
        }
}
```
