# Kubernetes

Lugar donde vamos a guardar comandos de kubernetes.

En el segmiento de abajo podemos observar un ejemplo para levantar un docker para luego usar en nuestro lab de K8s.

```
#Clonamos el repo
git clone https://github.com/platzi/curso-kubernetes/

#Modificamos el Dockerfile
vim curso-kubernetes/dockercoins/webui/Dockerfile
    FROM node:4-slim
    RUN npm install express
    RUN npm install redis@2.8.0
    COPY files/ /files/
    COPY webui.js /
    CMD ["node", "webui.js"]
    EXPOSE 80

#Levantamos el docker
docker compose up
```

