# MÓDULO DE Docker_Container EN ANSIBLE


![Docker and Ansible](https://miro.medium.com/v2/resize:fit:693/1*Rf4daxtM_oOSR1g187FIiA.jpeg)

## Introducción

- El módulo **docker_container** de Ansible gestiona contenedores Docker, permitiendo crearlos, iniciarlos, detenerlos o eliminarlos, con opciones para configurar puertos, volúmenes y políticas de reinicio. Asegura que el contenedor esté siempre en el estado deseado.

***

## Requisitos : 

Docker: Instalado en el servidor de destino.
Python y Docker SDK: **pip install docker**.
Permisos: Acceso al Docker socket (/var/run/docker.sock).
Ansible: Instalado en el nodo de control.


*** 

## Preparacion de Entorno : 


- Este playbook instala Docker, inicia el servicio .
![Docker and Ansible](/img/1.png)


### EJECUCIÓN DEL PLAYBOOK

![Docker and Ansible](/img/2.png)

***

## Ejemplos de Funcionamiento

### Ejemplo 1 : Desplegar contenedor Nginx con docker_container 

- Este playbook de Ansible despliega un contenedor Nginx usando Docker, nombrado "mi-nginx", basado en la imagen "nginx:latest", y lo expone en el puerto 8080 del host.

![Docker and Ansible](/img/3.png)


- Ejecución de un Playbook de Ansible para Desplegar Nginx en Docker


![Docker and Ansible](/img/4.png)

### Comprobacion : 

![Docker and Ansible](/img/5.png)
![Docker and Ansible](/img/6.png)


***

### Ejemplo 2 : Desplegar MySQL con docker_container

- Este playbook despliega un contenedor MySQL 5.7 usando Docker, establece variables de entorno como la contraseña de root y la base de datos, y mapea el puerto 3306 del contenedor al host.

![Docker and Ansible](/img/7.png)


- Ejecución de un Playbook de Ansible para Desplegar la base de datos MySQL en Docker

![Docker and Ansible](/img/8.png)

### Comprobacion : 

![Docker and Ansible](/img/9.png)


![Docker and Ansible](/img/10.png)



***

### Ejemplo 3 : Gestionar estados de contenedores con docker_container (docker stop $container)


- Este playbook gestiona los estados de los contenedores Docker, deteniendo el contenedor mi-nginx y eliminando el contenedor mi-mysql.

![Docker and Ansible](/img/11.png)


- Ejecución de un Playbook de Ansible para detener el contenedor mi-mynignx y borrar mysql

![Docker and Ansible](/img/12.png)


### Comprobacion : 
![Docker and Ansible](/img/13.png)



***

## Referencias : 

[Medium.com : Docker containers with Ansible ](https://medium.com/@Oskarr3/docker-containers-with-ansible-89e98dacd1e2)

[Reddit.com : Understanding Ansible in Docker containers ](https://www.reddit.com/r/ansible/comments/1clwion/understanding_ansible_in_docker_containers/)
