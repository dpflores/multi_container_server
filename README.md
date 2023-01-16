## Los tres juntos

Para correr los tres servicios, solo descomente la parte de nodered en docker-compose.yml, cabe mencionar que tiene que colocar la image con la aplicacion final que se quiera implementar o cuando hagamos docker compose down, estos no se guardaran. 

```
docker compose up
```

## mariadb y phpmyadmin

si queremos solo correr estos dos, cosa que el nodered no se reinicie cada vez que hagamos el docker-compose down, entonces solo comentamos la parte de nodered en el archivo y para realizar aplicaciones de nodered en un contenedor que posteriormente podamos guardar como imagen y que sirvan para el docker-compose.yml final luego de levantar los dos servicios, podemos ejecutar 


docker run --name nodered_container --network host nodered/nodered

podemos usar una imagen que tal vez tenga ya todo instalado y facilitarnos algunos pasos.

Una vez que tengamos ya el contenedor con el sistema finalizado, lo podemos guardar como una imagen.

docker commit <nombre del contenedor> <nombre de la imagen>

con ello, hemos creado la imagen que posteriormente se puede poner en el .yml para tener nuestra aplicación completa.
