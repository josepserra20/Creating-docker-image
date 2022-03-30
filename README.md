Práctica realizada por Alessandro Lapini y Josep Serra

# Creando una imagen personalizada para la API REST con Flask y Mongo Atlas en Docker

Partimos de nuestro proyecto Ollivanders inspirado en el Kata **Gilded Rose**. Todos los pasos anteriores al dockerfile ya los teníamos realizados en el proyecto ya que eran un requisito. Así que comenzaremos por el dockerfile.

### Dockerfile

Así debemos configurar el archivo *Dockerfile* para empezar con nuestra imagen personalizada. Deberemos añadir los comandos necesarios para que ejecute la app en el contenedor cuando se corra la imagen.

![dockerfile](/images/dockerfile.PNG)

Una vez tengamos el dockerfile procedemos a loggearnos en **DockerHub** para así subir la imagen a nuestro perfil. 

Tras haber iniciado sesión volvemos al proyecto y ejectuamos el siguiente comando

``` 
docker build -t ollivander 
```

Esto es lo que nos aparecerá en la terminal

![docker_build](/images/build.PNG)

Para confirmar que hemos creado la imagen ejecutamos el siguiente comando

``` 
docker images
```

El output debería ser el siguiente:

![docker_images](/images/images.PNG)

Ahora vamos a iniciar sesión por consola a dockerhub. Aquí cada uno tendrá que escribir sus credenciales.

``` 
docker login
```

Ahora vamos a "taggear" (marcar) nuestra imagen antes de subirla a nuestro perfil. La convención de Docker es "account name/image name".

``` 
docker push accname/ollivander:latest
```
![docker_profile](/images/tag.PNG)

Al acceder a nuestro perfil web de dockerhub veremos nuestra imagen personalizada.

![docker_push](/images/vpsuh.PNG)

![docker_run](/images/docker-run.PNG)