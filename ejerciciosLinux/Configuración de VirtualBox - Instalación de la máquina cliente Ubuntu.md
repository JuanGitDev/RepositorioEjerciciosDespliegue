# Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu 

[TOC]

## 1 - Configuración de VirtualBox

Lo primero es escoger el modo _Experto_ en las preferencias de VirtualBox

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919104535517.png" alt="image-20250919104535517" style="zoom:67%;" />

Vamos a añadir una red tipo NAT para poder conectar varias maquinas virtuales

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919104748639.png" alt="image-20250919104748639" style="zoom:67%;" />

De damos a crear, luego le cambiamos el nombre y modificamos la IP

![image-20250919105357122](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919105357122.png)

<div style="page-break-after: always;"></div>
## Creación de la nueva máquina Cliente Ubuntu

Establecemos los parámetros de la maquina nueva

![image-20250919110054627](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919110054627.png)

Modificamos la RAM y subimos a 4GB y cambiamos a 4CPUs

![image-20250919110703442](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919110703442.png)

Cambiamos a 40GB de almacenamiento

![image-20250919110801636](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919110801636.png)

Le damos a terminal luego

![image-20250919110838387](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919110838387.png)



Cambiaremos ahora algunos ajustes:

- Nos vamos a **configuración -> descripción** guardamos el usuario y contraseña para acordarnos de ella

![image-20250919111115129](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919111115129.png)

- Si necesitas grabar cosas con ella le desactivas el audio

![image-20250919111515152](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919111515152.png)

- El adaptador de red lo cambiamos con el que creamos anteriormente, en este caso Red Nat y le damos **Aceptar**

![image-20250919111823018](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919111823018.png)

> Configuración finalizada, ya podemos inicial la maquina 
> 
<div style="page-break-after: always;"></div>
## 3 - Instalación de la maquina virtual

Nos van apareciendo distinta opciones

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919120918725.png" alt="image-20250919120918725" style="zoom:67%;" />

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919121047526.png" alt="image-20250919121047526" style="zoom:67%;" />

Buscamos el nombre que habíamos guardado en descripción y usamos la misma contraseña que tenemos

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919121331723.png" alt="image-20250919121331723" style="zoom:67%;" />

Damos siguiente hasta el final y dejamos que termine de instalarse

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919121459121.png" alt="image-20250919121459121" style="zoom:67%;" />

Al finalizar damos click en reiniciar y ya puedes usar linux

<img src="./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919123053537.png" alt="image-20250919123053537" style="zoom:67%;" />



## 4 - Instalación de los Guest Aditions

Ya iniciada la maquina virtual nos vamos a dispositivos y de damos a insertar imagen de CD

![image-20250919124407413](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919124407413.png)

Ahora nos vamos al explorador de archivos de la maquina virtual y le damos en ejecutar programa e introducimos la contraseña cuando la pida

![image-20250919124622459](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919124622459.png)

Nos dará un error

![image-20250919124715561](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919124715561.png)

Usaremos el siguiente comando en la consola de comandos

```
sudo apt install bzip2 tar
```

Nos pedirá la contraseña, ingresamos

![image-20250919125001806](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250919125001806.png)

Luego ingresamos el siguiente comando

```
sudo apt install virtualbox-guest-utils
```

Y ejecutamos

![image-20250924094723316](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250924094723316.png)

También ejecutamos el siguiente comando:

```
sudo usermod -aG vboxsf cliente
```

![image-20250924094949276](./Configuración de VirtualBox - Instalación de la máquina cliente Ubuntu.assets/image-20250924094949276.png)

