# MySql Ubuntu 22.04
Guía para instalar y configurar MySql en un servidor privado virtual que ejecuta la distribución Ubuntu. Requiere usuario 'root'.

## Instalación

Primero actualizaremos e instalaremos paquetes nuevos. Para ello ejecutaremos los siguientes comandos:

```bash
sudo apt update
```
```bash
sudo apt upgrade
```
Después de actualizar los paquetes procederemos a instalar MySql con los siguientes comandos:

```bash
sudo apt install mysql-server
```
Durante la instalación tendremos que confirmar algunos cambios. Para ello escribiremos 'Y' en la terminal cuando nos pida.

Una vez terminado la instalación de MySql procederemos a verificar si está funcionando correctamente con el siguiente comando:
```bash
sudo systemctl status mysql
```
Si nos sale un mensaje igual que el siguiente, la Instalación fue correcta. Cerramos el mensaje presionando las teclas "Ctrl + C" a la vez.

![](images/status.png)


## Configurar MySQL 
Entramos a MySQL escribiendo el siguiente comando en la terminal.
```bash
mysql
```
Crearemos un nuevo usuario en MySQL con todos los permisos para evitar usar el usuario root. Para ello ejecutamos los siguientes comandos:
```bash
create user 'tuusuario'@'%' identified by 'tucontraseña';
```
Reemplaza por tu usuario y tu contraseña. No elimines los apostrofes ( ' ).

Daremos todos los permisos con los siguientes comandos:
```bash
grant all privileges on *.* to 'tuusuario'@'%' with grant option;
```
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)