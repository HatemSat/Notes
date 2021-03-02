# Notes

## Unix
* Copy current folder tree with only .env files for machine migration : `sudo find . -name '*.env' | sudo cpio -pdm  env_backup/`

## Firebase

1. Initialisation et commandes de base d'un projet functions :  
   Suppréssion : `firebase functions:delete {nom fonction} [--region {europe-west1}]` Mode intéractif nécéssaire pour confirmmer sinon utiliser `--force`

2. Variables d'environement cloud functions :  
   Déclaration : `firebase functions:config:set foo.url="value" foo.key="123"`  
   Lecture : `firebase functions:config:get`  
   Suppréssion : `firebase functions:config:unset foo.key`

## Wndows

1. Conversion gif vers webm `ffmpeg -i my-animation.gif -c vp9 -b:v 0 -crf 41 my-animation.webm`

## Nginx

1. Cache
    - La compréssion Gzip supprime les Etag (fingerprint des ressources) et empêche donc la gestion du cache :
    ```
        location / {
                gzip off;
                etag on;
                ...
    ```
## PM2
1. Commandes de base : 
   ```
   pm2 delete,start,restart {app-ame} || {id} || all
   pm2 list || status
   pm2 describe {id} || {app-name}
   pm2 logs
   pm2 monit
   ```
2. Watch for changes and reload (ignore modules) : `pm2 start env.js --watch           --ignore-watch="node_modules"`
