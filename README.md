# servidor-web-dockerizado-Nginx


 
Lo primero de todo descargaremos el docer desde su pagina principal en mi caso es version para window con interfaz grafica.

![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.1.png)
![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.2.png)

Ahora vamos al docker hub para descargar el imagen de nginx(necesita registracion).

![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.3.png)

Con el comando dado ejecutaremos en el terminal y obtendremos el nginx en el docker.

![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.4.png)
![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.5.png)

Lo siguiente es usar el siguiente comando para poner el web en puerto 8080 y con el nombre de contenedor
~~~
docker run --rm -d -p 8080:80 --name miweb nginx
~~~

![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.6.png)
![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.7.png)

Y lo paramos para agregar mi pagina web con el comando o usar interfaz grafico.
~~~
docker stop miweb 
~~~

Ya he creado mi pagina web lo agregamos al nginx dockerizado con el comando. C:\Users\Usuario\Documents\nginx\web es donde esta el web 
~~~
docker run --rm -d -p 8080:80 --name miweb -v C:\Users\Usuario\Documents\nginx\web:/usr/share/nginx/html nginx
~~~

![](https://github.com/ZhijunLin7/servidor-web-dockerizado-Nginx/blob/main/Camera%20Roll/1.8.png)
