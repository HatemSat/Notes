# Notes

## Firebase
* Initialisation et commandes de base d'un projet functions :  
Suppréssion : `firebase functions:delete {nom fonction} [--region {europe-west1}]` Mode intéractif nécéssaire pour confirmmer sinon utiliser `--force`

* Variables d'environement cloud functions :  
Déclaration : `firebase functions:config:set foo.url="value" foo.key="123"`  
Lecture : `firebase functions:config:get`  
Suppréssion : `firebase functions:config:unset foo.key`

