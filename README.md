# Acceso seguro en Nginx con Docker

## Configuración básica de Nginx
![Imagen de configuración básica de Nginx](./img/001.png)

## Generar certificado autofirmado

### Instalación de paquetes necesarios
Realizado en la [práctica anterior](https://github.com/Dani-Ba-2DAW/Nginx-Docker-Autenticacion#instalaci%C3%B3n-de-paquetes-necesarios).

### Generar certificado
¡Recuerda cambiar "~" por "C:/Users/[usuario]" si estás en Windows!<br><br>
¡Importante, no se genera un .crt, se va a usar el .pem que genera!<br><br>
Comando: docker run --rm -e SSL_SUBJECT=dani.test -e SSL_KEY_SIZE=2048 -e SSL_DAYS_VALID=365 -v ~/certs:/certs stakater/ssl-certs-generator:latest

![Imagen de generar certificado](./img/002.png)

## Configuración

![Imagen de configuración](./img/003.png)