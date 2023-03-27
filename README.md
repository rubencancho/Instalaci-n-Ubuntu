# Instalación de Ubuntu

## Que es Ubuntu?

Ubuntu es una distribución Linux basada en Debian GNU/Linux, que incluye principalmente software libre y de código abierto.

Puede utilizarse en ordenadores y servidores. Está orientado al usuario promedio, con un fuerte enfoque en la facilidad de uso y en mejorar la experiencia del usuario. Está compuesto de múltiple software normalmente distribuido bajo una licencia libre o de código abierto. Estadísticas web sugieren que la cuota de mercado de Ubuntu dentro de las distribuciones Linux es, aproximadamente, del 52 %, y con una tendencia a aumentar como servidor web. 

# Proceso de instalación

## Instalación de Virtualbox

Descargaremos [Virtualbox](https://www.virtualbox.org/) para el sistema operativo de nuestro ordenador.

## Configuración de Virtualbox

Arrancamos Virtualbox y hacemos click en "Nueva":

![Virtualbox1](./virtualbox1.png)

Escribimos el nombre de la máquina virtual, en nuestro caso "Ubuntu". Vemos que se selecciona automáticamente el tipo de sistema a "Linux" y la versión a "Ubuntu 64-bit".

![Virtualbox2](./virtualbox2.png)

Configuramos el tamaño de memoria para la máquina virtual. Para Ubuntu 22.04 se recomiendan 4GB (4096MB):

![Virtualbox3](./virtualbox3.png)

Creamos un nuevo disco duro virtual:

![Virtualbox4](./virtualbox4.png)

Elegimos del tipo de disco duro virtual de tipo VDI (Virtual Disk Image):

![Virtualbox5](./virtualbox5.png)

Le indicamos que el fichero del disco duro virtual crezca dinámicamente, a medida que necesitemos más espacio:

![Virtualbox6](./virtualbox6.png)

Configuramos el tamaño del disco duro virtual a 25GB, ya que es el tamaño recomendado en la instalación de Ubuntu 22.04:

![Virtualbox7](./virtualbox7.png)

Ya tenemos creada la máquina virtual, solo nos falta introducir el disco virtual del sistema operativo:

![Virtualbox8](./virtualbox8.png)

Nos descargamos previamente el archivo ISO de la distribución Linux que queramos. En nuestro caso hemos elegido la distribución [Ubuntu](https://ubuntu.com/), en su versión 22.04.

El siguiente paso es "montar" la ISO en el lector virtual de la máquina virtual. Para ello hacemos click en "Configurar y posteriormente vamos a la sección "Almacenamiento":

![Virtualbox9](./virtualbox9.png)

Hacemos click en "Vacío" dentro del árbol "Controlador IDE", y posteriormente elegimos el archivo ISO desde el icono de "Unidad Óptica":

![Virtualbox10](./virtualbox10.png)

Antes de arrancar configuramos la memoria de la tarjeta de vídeo al máximo posible, dentro de "Configuración" -> "Pantalla":

![Virtualbox11](./virtualbox11.png)

Por último la damos a "Iniciar" en la máquina virtual y vemos como empieza a arrancar:

## Instalación de Ubuntu

Vemos la pantalla de Grub y elegimos la opción "Try or Install Ubuntu", y le damos a la tecla "Enter":

![Ubuntu1](./ubuntu1.png)

Elegimos el idioma y hacemos click en "Instalar Ubuntu":

![Ubuntu2](./ubuntu2.png)

Elegimos la distribución de teclado:

![Ubuntu5](./ubuntu5.png)

Elegimos el tipo de instalación. En nuestro caso instalación mínima y le indicamos que instalaremos software de terceros:

![Ubuntu6](./ubuntu6.png)

Elegimos borrar todo el disco y que se instale Ubuntu como único sistema operativo:

![Ubuntu7](./ubuntu7.png)

# Actualización del sistema

## Actualización desde linea de comandos

Para actualizar el sistema desde linea de comandos abriríamos una terminal (Gnome-Terminal) y escribiríamos los siguientes comandos:

1. Actualizamos los índices de paquetes:

```
sudo apt update
```
![actualizacion_apt_1](https://user-images.githubusercontent.com/79692984/227209399-d76be58f-114d-4a69-8514-dddad1ccc610.png)


2. Vemos la lista de paquetes que se pueden actualizar:

```
apt list --upgradable
```
![actualicacion_apt_2](https://user-images.githubusercontent.com/79692984/227209547-aa9977dc-1b85-4924-b523-cef8275dac3a.png)

3. Actualizamos los paquetes instalados que tienen nuevas versiones en los repositorios:

```
sudo apt upgrade
```
![actualizacion_apt_3](https://user-images.githubusercontent.com/79692984/227209611-d4232a4e-9984-4bd5-b543-6596b4161eaf.png)



## Actualización desde el interfaz gráfico

Abrimos la aplicación "Software Updater".
![actualizacion_grafica_1](https://user-images.githubusercontent.com/79692984/227210929-21e55aca-f4b7-491a-87a6-4d67747e4260.png)

Vemos como el "Software Update" comprueba las actualizaciones:
![actualizacion_grafica_2](https://user-images.githubusercontent.com/79692984/227211023-afe0cfca-a6a8-4d13-846c-a411d969dc04.png)

"Software Updater" nos informa de las actualizaciones y nos pregunta si queremos actualizar:
![actualizacion_grafica_3](https://user-images.githubusercontent.com/79692984/227211154-05b188f8-782a-442f-979f-ed29b7be1c67.png)

Por último se instalan las actualizaciones y debemos reiniciar el ordenador si nos lo pidiera:
![actualizacion_grafica_4](https://user-images.githubusercontent.com/79692984/227211547-4609352e-5c34-489b-82c0-73686b8917a1.png)


# Instalación de software

Vamos a instalar la herramienta OBS Studio. Para ello seguiremos los pasos de la página web.

En primer lugar instalamos los paquetes que necesita OBS, en concreto el paquete ffmpeg:

```
sudo apt install ffmpeg
```
![instalacion_2](https://user-images.githubusercontent.com/79692984/227881888-fb3eaf08-9772-45e4-8a8e-37e69e6fd838.png)


En segundo lugar nos dicen que añadamos el repositorio externo mediante la linea de comandos:

```
sudo add-apt-repository ppa:obsproject/obs-studio
```
![instalacion_3](https://user-images.githubusercontent.com/79692984/227883116-162e6062-9808-4f43-bcb0-f1ae4891d056.png)

En tercer lugar actualizamos los índices de todos los repositorios:

```
sudo apt update
```

Por último instalamos OBS Studio:

```
sudo apt install obs-studio
```
![instalacion_5](https://user-images.githubusercontent.com/79692984/227884996-e4bc0ab4-ad92-4bf7-a735-862212d387a2.png)





## Mediante la herramienta synaptic

En primer lugar debemos comprobar que tenemos la herramienta instalada, podemos usar la siguiente linea de comandos para instalarla:

```
sudo apt install synaptic
```
![instalacion_1](https://user-images.githubusercontent.com/79692984/227879851-ebc011ea-b606-45ca-b3a8-6cc9196a50cc.png)

##




# Referencias

- "Ubuntu". Wikipedia. Disponible en: [https://es.wikipedia.org/wiki/Ubuntu](https://es.wikipedia.org/wiki/Ubuntu)  (Accedido: 6 de marzo, 2023).
