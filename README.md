# API Documentation

## Set Login Code
**Endpoint:** `https://api-p.pylote.io/freelance/set_login_code`  
**Method:** POST  

**Request Body:**
```json
{
  "mail": "example@example.com",
  "resend": false
}
```
**Description:** Permet de demander le code pour se connecter.

## Check Code
**Endpoint:** `https://api-p.pylote.io/freelance/check_code`  
**Method:** POST  

**Request Body:**
```json
{
  "mail": "example@example.com",
  "code": "123456"
}
```
**Description:** Vérifie si le code est correct.

## Get Jobs
**Endpoint:** `https://api-p.pylote.io/jobs/`  
**Method:** GET  

**Description:** Permet d'obtenir la liste des jobs.

## Set Availability
**Endpoint:** `https://api-p.pylote.io/availability/{id}`  
**Method:** PUT  

**Request Body:**
```json
{
  "available": true,
  "availabilityDate": "2024-06-18"
}
```
**Description:** Permet de définir la disponibilité actuelle. Mettre une chaîne vide dans `availabilityDate` s'il n'y en a pas.

## Update Logs
**Endpoint:** `https://api-p.pylote.io/logging/update`  
**Method:** POST  

**Request Body:**
```json
{
  "id": "123",
  "variable": "availability",
  "value": "ldzsd"
}
```
**Description:** Permet de mettre à jour les logs pour la disponibilité.

## Get Logs
**Endpoint:** `https://api-p.pylote.io/logging/getLogs/{id}`  
**Method:** GET  

**Description:** Permet de récupérer les logs du compte.

## Get Recruiters
**Endpoint:** `https://api-p.pylote.io/recruiter/`  
**Method:** GET  

**Description:** Permet d'obtenir la liste des recruteurs. Possibilité de rajouter `?displayMissions=true` à l'URL.

## Get Profile
**Endpoint:** `https://api-p.pylote.io/freelance/profile/{id}`  
**Method:** GET  

**Description:** Permet d'obtenir le profil de l'utilisateur.

## Update Profile
**Endpoint:** `https://api-p.pylote.io/freelance/update_profile_head/{id}`  
**Method:** POST  

**Description:** Permet de modifier le profil de l'utilisateur. Doit mettre à jour la variable `j` pour le fonctionnement.

## Update description profile
**Endpoint:** `https://api-p.pylote.io/freelance/update_profile_description/`

**Method:** POST


**Description:** Permet de modifier la description de l'utilisateur. Doit mettre à jour la variable j

## Update profile preference

**Endpoint:** `https://api-p.pylote.io/freelance/update_profile_preferences/`

**Method:** POST


**Description:** Permet de modifier les préférences du profil
```json
{ 
  "daysPerWeek":"Indifférent",
  "missionDuration":"Indifférent",
  "location":
    {
      "description":"Lille, France",
      "id":"ChIJEW4ls3nVwkcRYGNkgT7xCgQ"
    },
  "remoteWork":["Télé-travail"],
  "workAreas": [
    {"type":"ville",
    "code":"59000",
    "label":"Lille",
    "regionName":"Hauts-de-France"
  }],
  "vehicle":false
```

 
## Get possible preference
**Endpoint:** `https://lbzunxli1l.execute-api.eu-west-3.amazonaws.com/default/lambda-pylote-input-prod`

**Method:** POST

**Possible fields:** DaysPerWeek, MissionDuration, RemoteWork, Mobilities.

```json
{
 "action": "list:all",
 "field": ""
}
```
 
## Get autocomplete of location

**Endpoint:** `https://api-p.pylote.io/locations/autocomplete?q= + la query`

**Method:** GET


**Description:** Permet d'avoir les locations qu'ont pylote dans leur api. Utile pour avoir l'id de la ville pour l'update de préférence 
