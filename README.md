# Mampp - Vagrant
Servidor web en ubuntu 16.04.3 al completo.
Mampp (My Apache MariaDB phpMyAdmin Perl), con el podras tener todo lo necesario para testear cualquier aplicación web.

USO
===
Instalación (Pondre la version de los programas por posible errores futuras)
---
1. Instalar VirtualBox `(v5.1.28 r117968)`
2. Instalar Vagrant `(v2.0.0)`

Despues de las instalaciones lanzamos este comando en el CMD
```
vagrant plugin install vagrant-vbguest
```
3. Descargaremos el repositorio y lo movemos a tu carpeta de usuario.
4. Nos movemos a dicha carpeta desde el CMD
5. Lanzaremos el siguiente comando:
```
vagrant up
```
6. En tu archivo host de windows (C:\Windows\System32\drivers\etc\hosts) añadiremos la siguiente linea:

windows: 
  *`192.168.1.10           mampp.dev`
  *`192.168.1.10           vagrant.dev`
Linux:
  *`................`

(Asi podras utilizar los dominios virtuales que he creado dentro)

Dominios

*`mampp.dev   ......................................   Info de Apache2`
*`mampp.dev/phpmyadmin   ...........................   Web phpMyAdmin`
    USER:     root
    PASSWD:   vagrant
*`vagrant.dev   ....................................   Dominio enlazado a la raiz de la web`

Box
---
Esta totalmente creada y editada por mi, ni necesitais y creis que es necesario algun servicio adicional decirmelo.
