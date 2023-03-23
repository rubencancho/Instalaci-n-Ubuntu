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


```
sudo apt update
```

## Actualización desde el interfaz gráfico


# Referencias

- "Ubuntu". Wikipedia. Disponible en: [https://es.wikipedia.org/wiki/Ubuntu](https://es.wikipedia.org/wiki/Ubuntu)  (Accedido: 6 de marzo, 2023).
