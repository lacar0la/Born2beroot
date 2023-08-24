# Born2beroot
In this project we work on virtual machines and operating systems. 
Next I share some of my study notes for the project, A virtual machine for installing debian 10 was made, that's why some commands are for linux systems.
like before, all my notes are in spanish. 


# Born2beRoot -42

A continuación, comparto mis apuntes sobre este proyecto.

# Virtualbox

Es un software de virtuaizaciòn desarrollado por Oracle corporation que permite, crear y ejecutar máquinas virtuales en un sistema operativo host.

Una **máquina virtual** es un entorno informático completo y aislado que funciona dentro de otro sistema operativo. Esto significa que puedes tener múltiples sistemas operativos, como Windows, Linux, macOS u otros, funcionando simultáneamente en un mismo ordenador, sin afectar el sistema operativo principal.

VirtualBox **es gratuito** y está disponible para múltiples sistemas operativos, lo que lo hace una opción popular y accesible para la virtualización en entornos personales y profesionales. Además, cuenta con una comunidad activa que ofrece soporte y recursos adicionales para su uso y configuración.

---

# ¿Qué es una máquina virtual?

Una máquina virtual (VM, por sus siglas en inglés) es un entorno de software que emula una computadora completa y funcional dentro de otra computadora física o anfitrión. Es una técnica de virtualización que permite ejecutar múltiples sistemas operativos y aplicaciones independientes en un solo hardware físico.

En esencia, una máquina virtual simula los componentes de una computadora física, como procesador, memoria, almacenamiento, red y otros dispositivos, y permite que un sistema operativo y sus aplicaciones se ejecuten de manera aislada dentro de ese entorno virtual. Cada máquina virtual se comporta como una entidad independiente con su propio sistema operativo, software y configuración.

Las máquinas virtuales son creadas y gestionadas por un software de virtualización, que se conoce como "hipervisor" o "monitor de máquina virtual". El hipervisor es responsable de alojar y administrar las máquinas virtuales, así como de asignar los recursos físicos del host entre las máquinas virtuales.

**Imagen del sistema operativo:** Se necesita una imagen del sistema operativo que desees ejecutar en la máquina virtual. Esta imagen se instala dentro de la VM y contiene todos los archivos y configuraciones necesarios para que el sistema operativo funcione.

# Sistemas operativos

Para este proyecto debes instalar una ISO de un sistema operativo en tu maquina virtual. El tutorial recomienda instalar DEBIAN, pero este no es el unico sistema operativo que existe, tambien está Solaris, Genode, GNU linux, entre otros.

- Solaris:

Solaris es un sistema operativo tipo Unix, es conocido por su robustez, escalabilidad y capacidad para ejecutarse en grandes sistemas de servidor. Solaris ha sido ampliamente utilizado en entornos empresariales y de alto rendimiento debido a su confiabilidad y características avanzadas

- Debian:

Debian es un sistema operativo libre y de código abierto basado en el núcleo de Linux. Es conocido por su enfoque en la estabilidad, seguridad y su **comunidad de desarrollo activa**. Debian utiliza el sistema de gestión de paquetes APT (Advanced Package Tool) para facilitar la instalación y actualización de software de manera sencilla y segura. 

Una de las características más destacadas de Debian es su amplia gama de arquitecturas de hardware soportadas, lo que lo hace adecuado para ejecutarse en diversos dispositivos y entornos, desde computadoras de escritorio y portátiles hasta servidores y sistemas embebidos.

---

# Aptitude - APT

APT Y Aptitude son gestores de paquetes de software que permiten realizar un manejo de la información dentro del ordenador, ambos son gestores basados en debian y su elección depende mucho de las caracteristicas especificas, requerimientos del usuario, conocimiento del usuario, etc. 

En este caso

**Aptitude**

- Proporciona una interfaz avanzada e interactiva
- Soporte para multiples metodos de instlación
- Permite navegar por los paquetes, buscar información detallada, ver las dependencias
- Resuelve automaticamente las dependencias, es mucho mas eficiente para la resolución de conflictos.
- Matiene un registro mas detallado de las acciones en el sistema

**APT**

La interfaz es mucho mas moderna y amigable

Combina funcionalidad de apt-get y apt cache

La sintaxis requerida es mucho mas sencilla

Puede resolver dependencias, sin embargo si hay un conflictoi requeriá la ayuda del usuario.

No tiene historial completo de las acciones

Comandos sencillos y faciles de recordar

**APT es el sistema centralizado y eficiente para la instalación, actualización y eliminación de software en estos sistemas**

Las principales componentes de APT incluyen:

1. **apt-get:** Esta es una de las utilidades más conocidas de APT. Permite realizar tareas como instalar paquetes, actualizar la lista de paquetes disponibles, realizar actualizaciones de sistema, y mucho más.
2. **apt-cache:** Permite gestionar la caché local de información de paquetes, como buscar información sobre paquetes disponibles y mostrar detalles sobre un paquete específico.
3. **aptitude:** Como mencioné anteriormente, aptitude es otra herramienta de gestión de paquetes que utiliza la infraestructura de APT. Proporciona una interfaz interactiva para la administración de paquetes.
4. **apt:** Es una interfaz más moderna y amigable para usar APT. A diferencia de las herramientas anteriores, "apt" no requiere que uses comandos separados como "apt-get" y "apt-cache". En su lugar, combina estas funciones en una sola interfaz.
5. **dpkg:** Aunque no es parte directa de APT, dpkg es la herramienta de bajo nivel que APT utiliza para instalar y administrar paquetes individuales. APT se encarga de gestionar las dependencias y de brindar una interfaz más fácil de usar para dpkg.

---

# SELinux

SELinux, significa Security-Enhanced Linux **(Linux con Seguridad Reforzada)**, es un marco de seguridad para sistemas Linux que proporciona mecanismos de control de acceso obligatorio (MAC) para aplicar controles y políticas de acceso detallados en diversos recursos del sistema.

El objetivo principal de SELinux es controlar las acciones que los procesos y los usuarios pueden realizar en los recursos del sistema, basándose en políticas de seguridad definidas por los administradores del sistema. Esto se logra etiquetando archivos, procesos y recursos de red con etiquetas de contexto de seguridad, que luego se utilizan para determinar si una operación en particular está permitida o denegada según las políticas definidas.

# AppArmor

AppArmor es un sistema de control de acceso obligatorio (MAC) para sistemas Linux que se utiliza para limitar y controlar los recursos a los que pueden acceder las aplicaciones y procesos en un sistema. Similar a SELinux, AppArmor es una herramienta de seguridad que agrega una capa adicional de protección al sistema operativo y ayuda a prevenir posibles vulnerabilidades y ataques al restringir el acceso de las aplicaciones solo a los recursos que necesitan para funcionar correctamente.f

La principal función de AppArmor es definir y aplicar políticas de seguridad que especifiquen qué acciones están permitidas para cada aplicación o proceso. Esto se logra mediante la creación de perfiles de seguridad para aplicaciones individuales, que contienen las reglas que determinan qué archivos, directorios, operaciones de red y otros recursos pueden ser accedidos por esa aplicación en particular. AppArmor utiliza estas políticas para hacer cumplir las restricciones de acceso y evitar que una aplicación acceda a recursos no autorizados.

# GID

Es el identificador de grupo, es una abreviatura de Group ID

## Comprobación de grupos

Lo cierto es que si ya que no ha habido ningún mensaje de error, aún así podemos comprobar si se ha creado con el comando `getent group nombre_grupo` o también podemos hacer `cat /etc/group` y podremos ver todos los grupos y los usuarios que hay dentro de ellos.

# SSH

SSH (Secure Shell) es un protocolo de red que permite la comunicación segura y encriptada entre dos dispositivos, generalmente utilizado para acceder de forma remota a un sistema o servidor de manera segura. También se refiere al programa informático que implementa este  protocolo y proporciona una interfaz para realizar conexiones SSH.

SSH fue diseñado como una alternativa segura a los antiguos protocolos de acceso remoto, como Telnet, que transmitían datos en texto claro, lo que los hacía susceptibles a ataques de interceptación y robo de información confidencial, como contraseñas. En cambio, SSH utiliza técnicas de cifrado para asegurar que los datos transmitidos entre el cliente y el servidor estén protegidos de miradas indiscretas.

El funcionamiento básico de SSH es el siguiente:

1. Un cliente SSH se conecta a un servidor SSH.
2. El servidor autentica al cliente, lo que generalmente implica que el cliente debe proporcionar credenciales (nombre de usuario y contraseña) o una clave pública para demostrar su identidad.
3. Una vez autenticado, se establece una conexión cifrada entre el cliente y el servidor, lo que garantiza que cualquier dato transmitido entre ellos esté protegido de posibles ataques.

Es el nombre de un protocolo y del programa que lo implementa cuya principal función es el acceso remoto a un servidor por medio de un canal seguro en el que toda la información está cifrada.

# UFW

**UFW (Uncomplicated Firewall)** es una herramienta de configuración de firewall para sistemas operativos basados en Linux, diseñada para facilitar la administración y configuración del firewall de forma sencilla y rápida. UFW es una interfaz de usuario más simple y amigable para iptables, que es el sistema de firewall por defecto utilizado en muchas distribuciones de Linux.

I**ptables** es un programa de utilidad de espacio de usuario que permite a un [administrador de sistema](https://es.wikipedia.org/wiki/Administrador_de_sistemas) para configurar las [tablas](https://es.wikipedia.org/wiki/Tabla_(informaci%C3%B3n))[2](https://es.wikipedia.org/wiki/Iptables#cite_note-2) proporcionadas por el [cortafuegos del núcleo Linux](https://es.wikipedia.org/wiki/N%C3%BAcleo_Linux) (implementado como diferentes módulos [Netfilter](https://es.wikipedia.org/wiki/Netfilter)) y las cadenas y reglas que almacena. 

Se utilizan diferentes módulos del kernel y programas para protocolos diferentes; *iptables* se aplica a IPv4, *ip6tables* a IPv6, *arptables* a ARP, y *ebtables* a marcos de Ethernet.

# Comandos de configuración de la UFW

- **Passwd_tries=3:** Número de intentos en caso de introducir la contraseña erronea.
- **badpass_message=”Mensaje de error personalizado”:** Mensaje que se mostrará por pantalla en caso de que la contraseña introducida sea incorrecta.
- **logfile=”/var/log/sudo/sudo_config”** Activo en el que quedarán registrados todos los comandos sudo
- **log_input, log_output**
- **Iolog_dir =”var/log/sudo”** Para que cada comando ejecutado con sudo, tanto input como output quede archivado en el directorio especificado
- **************************************************Requiretty************************************************** Para activar el modo TTY
- **secure_path=”/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin”** Para restringir los directorios utilizables por sudo
    
    > *"sudo" es un comando que permite a los usuarios ejecutar tareas o comandos con privilegios de superusuario o administrador, también conocido como "root". El término "sudo" es una abreviatura de "SuperUser Do" (Hacer como superusuario).*
    > 
- **PASS_MAX_DAYS:** Es el tiempo de expiración de la contraseña. El numero corresponde a días.
- **PASS_MIN_DAYS:** El número mínimo de días permitido antes de modificar una contraseña.
- **PASS_WARN_AGE:** El usuario recibira un mensaje de aviso indicando que faltan los dias especificados para que expire su contraseña.
- **minlen=10:**  La cantidad minima de caracteres que debe contener la contraseña.
- **ucredit=-1** : Como mínimo debe contener una letra mayúscula. Ponemos el - ya que debe contener como mínimo un caracter, si ponemos + nos referimos a como maximo esos caracteres
- **dcredit=-1:** Como mínimo debe contener un digito.
- **lcredit=-1:** Como mínimo debe contener una letra minúscula.
- **maxrepeat=3**: No puede tener más de 3 veces seguidas el mismo caracter.
- **reject_username :** No puede contener el nombre del usuario.
- **difok=7:** Debe tener al menos 7 caracteres que no sean parte de la antigua contraseña.
- e**nforce_for_root:** Implementaremos esta política para el usuario root

# Particiones

En un disco duro o unidad de almacenamiento, se pueden crear varios tipos de particiones para organizar y gestionar el espacio disponible. Las particiones dividen el disco en segmentos separados, cada uno de los cuales puede ser utilizado para diferentes propósitos. Algunos de los tipos de particiones comunes son:

1. **Partición Primaria:** Es la partición principal en la que generalmente se instala el sistema operativo. Un disco duro puede tener hasta cuatro particiones primarias o tres particiones primarias y una partición extendida.
2. **Partición Extendida:** Es una partición especial que puede contener una o más particiones lógicas dentro de ella. Se utiliza cuando se requieren más de cuatro particiones en un disco. No almacena datos por sí misma, sino que actúa como un contenedor para particiones lógicas.
3. **Partición Lógica:** Son particiones creadas dentro de una partición extendida. No se pueden utilizar como particiones de arranque, pero son útiles para organizar y almacenar datos.
4. **Partición de Arranque (Boot Partition):** En sistemas con BIOS heredados, esta partición se utiliza para almacenar archivos de arranque del sistema operativo. En sistemas con UEFI, el arranque generalmente se maneja a través de particiones EFI.
5. **Partición del Sistema:** Contiene los archivos del sistema operativo y otros archivos esenciales para su funcionamiento.
6. **Partición de Datos:** Se utiliza para almacenar datos, archivos y programas. Estos datos no son necesarios para el arranque del sistema.
7. **Partición de Intercambio (Swap):** Utilizada como memoria virtual en sistemas Unix y Linux. Ayuda a liberar memoria RAM al mover datos inactivos de la memoria al espacio de intercambio en el disco.
8. **Partición de Recuperación:** A menudo creada por fabricantes de computadoras, esta partición contiene herramientas y archivos para restaurar el sistema a su estado original de fábrica.
9. **Partición de Respaldo (Backup Partition):** Reservada para copias de seguridad periódicas de datos importantes.
10. **Partición de Sistemas Múltiples:** En sistemas que admiten múltiples sistemas operativos, se pueden crear particiones para alojar diferentes sistemas operativos. Cada uno tiene su propio espacio y archivos.

En el proyecto tenemos 3 particiciones principales sda1, sda2 y sda5. La primera partición contiene la información del sistema, junto con los archivos de arranque.

La segunda partición es una partición especial que puede contener una o más particiones lógicas dentro de ella. Se utiliza cuando se requieren más de cuatro particiones en un disco. No almacena datos por sí misma, sino que actúa como un contenedor para particiones lógicas.

La ultima partición está encriptada y contiene otras separaciones internas, por ejemplo la partición swap como memoria virtual en sistemas Unix y Linux. Ayuda a liberar memoria RAM al mover datos inactivos de la memoria al espacio de intercambio en el disco.

# Script

<aside>
💡 Esta es una parte muy importante del proyecto. Debes prestar atención en todo, muy importante no copiar y pegar directamente el fichero sin saber que hace cada cosa. **En la evaluación debes explicar cada comando si el evaluador lo pide.**

</aside>

Un script es un archivo de texto que contiene una serie de instrucciones y comandos que se ejecutan de manera secuencial para realizar una tarea o un conjunto de tareas automatizadas en un sistema informático. 

Estas tareas pueden variar desde acciones sencillas hasta secuencias de comandos complejas, y su propósito es automatizar procesos y facilitar la ejecución de múltiples comandos sin necesidad de escribirlos cada vez que se desee realizar una acción específica.

Los scripts son ampliamente utilizados en diversos sistemas operativos y lenguajes de programación para una amplia variedad de propósitos, como:

1. Automatización de tareas: Los scripts pueden automatizar tareas repetitivas, lo que ahorra tiempo y reduce la posibilidad de errores humanos.
2. Administración del sistema: Los administradores de sistemas utilizan scripts para realizar tareas de mantenimiento, configuración y monitoreo de servidores y sistemas.
3. Procesamiento de datos: Los scripts pueden procesar datos en lotes, realizar transformaciones, filtrados o análisis en grandes conjuntos de datos.
4. Configuración de aplicaciones: Los scripts se utilizan para configurar y personalizar aplicaciones, estableciendo valores predeterminados o ajustando opciones específicas.
5. Implementación y despliegue de software: Los scripts son útiles en el proceso de implementación y despliegue de aplicaciones, automatizando la instalación y configuración de software.

## Architecture

```bash
uname -a ( "-a" == "--all" )
```

Este comando se usa para ver la arquitectura del Sistema Operativo SO. 

********************************************************************************************************************************************************************************************Muestra basicamente toda la información excepto si el tipo de procesador es desconocido.********************************************************************************************************************************************************************************************

![Esto esperamos ver](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/181c7542-a21b-453c-a372-a0bd40c97a05/Untitled.png)

Esto esperamos ver

---

## Núcleos

<aside>
💡 En un sistema operativo, el término "núcleo" se refiere a la parte central del sistema, que es responsable de gestionar y coordinar todos los recursos del sistema, permitiendo que los diferentes componentes y programas del sistema trabajen juntos de manera armoniosa. 

El núcleo es la parte esencial del sistema operativo y se ejecuta en modo kernel, lo que le brinda acceso directo a los recursos del hardware y la capacidad de gestionarlos de manera eficiente.

</aside>

Los principales roles y funciones del núcleo de un sistema operativo son los siguientes:

1. Administración de la memoria: El núcleo gestiona la memoria del sistema, asignando y liberando memoria para los programas y procesos en ejecución. También se encarga de proteger la memoria para evitar que un programa acceda indebidamente a la memoria asignada a otros procesos.
2. Planificación de procesos: El núcleo es responsable de planificar la ejecución de los diferentes procesos que se están ejecutando en el sistema. Utiliza algoritmos de planificación para determinar qué proceso se ejecutará en la CPU y durante cuánto tiempo, con el objetivo de optimizar el rendimiento y la eficiencia del sistema.
3. Administración de dispositivos: El núcleo controla y coordina el acceso a los dispositivos de hardware, como discos, impresoras, teclados, pantallas, etc. Se asegura de que los diferentes procesos y programas puedan utilizar los dispositivos de manera adecuada y sin conflictos.
4. Gestión de archivos: El núcleo proporciona una interfaz para acceder y administrar los archivos en el sistema de archivos. Se encarga de leer y escribir datos en los dispositivos de almacenamiento y garantizar que los archivos estén organizados y protegidos adecuadamente.
5. Gestión de red: En sistemas operativos modernos, el núcleo también se encarga de la gestión de la red, permitiendo la comunicación entre diferentes dispositivos y computadoras a través de la red.

Cabe mencionar que el núcleo del sistema operativo es la parte más crítica y sensible del sistema, ya que cualquier error o problema en el núcleo podría llevar a fallos graves del sistema. Por esta razón, el código del núcleo se desarrolla y mantiene con gran cuidado, y solo se permite el acceso y la modificación por parte de usuarios con privilegios especiales, como el usuario "root" en sistemas Unix/Linux o el administrador en sistemas Windows

---

## Núcleos físicos

Generalmente se refiere al componente central de un procesador o CPU (Unidad Central de Procesamiento). 

Un procesador es el cerebro de una computadora y está compuesto por uno o varios núcleos, que son unidades de procesamiento capaces de ejecutar instrucciones y realizar operaciones.

Cada núcleo físico es una unidad independiente de procesamiento que puede ejecutar tareas de manera simultánea. Los procesadores modernos suelen tener múltiples núcleos físicos en un solo chip para mejorar el rendimiento y la eficiencia. Esto permite que la CPU realice múltiples tareas al mismo tiempo, lo que es especialmente útil para aplicaciones que requieren un alto grado de procesamiento, como la edición de video, la renderización 3D y la ejecución de software complejo.

Para poder mostrar el numero de nucleos físicos haremos uso del fichero /proc/cpuinfo el cual proporciona información acerca del procesador: su tipo, marca, modelo, rendimiento, etc.

```bash
grep "physical id" /proc/cpuinfo | wc -l
```

Con el comando **grep** buscaremos dentro del fichero "physical id" y con **wc -l** contaremos las lineas del resultado de grep. 

El comando **`grep`** es una herramienta de búsqueda de patrones que permite buscar y filtrar líneas de texto que coinciden con un patrón específico dentro de uno o varios archivos o incluso en la entrada estándar. Su nombre proviene de "Global Regular Expression Print”

```css
grep [opciones] patrón [archivos...]
```

Donde:

- **`patrón`**: Es el texto o la expresión regular que se busca en el archivo o en la entrada estándar.
- **`[archivos...]`**: Es una lista opcional de archivos en los que se realizará la búsqueda. Si se omite, **`grep`** leerá la entrada estándar, lo que permite usar tuberías (pipes) para pasar la salida de otro comando como entrada.

Esto lo hacemos ya que la manera de cuantificar los nucleos no es muy común. 

Si hay un procesador marcará 0 y si tiene más de un procesador, mostrará toda la información del procesador por separado contando los procesadores usando la notación cero. De esta manera simplemente contaremos las lineas que hay ya que es más cómodo cuantificarlo así.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c6a3d6f5-00bb-4e3e-a9ab-2ef725b40bf4/Untitled.png)

## Núcleos virtuales

Para poder mostrar el numero de nucleos virtuales es muy parecido al anterior. Haremos uso de nuevo del fichero /proc/cpuinfo , pero, en este caso utilizaremos el comando:

```bash
grep processor /proc/cpuinfo | wc -l
```

El uso es practicamente el mismo al anterior solo que en vez de contar las lineas de "physical id" lo haremos de processor. Lo hacemos así por el mismo motivo de antes, la manera de cuantificar marca 0 si hay un procesador.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a5e33468-99c9-4558-8f55-c48fa9e65d5e/Untitled.png)

## Memoria RAM

Para mostrar la memoria ram haremos uso del comando `free` para así ver al momento información sobre la ram, la parte usada, libre, reservada para otros recursos, etc. Para más info sobre el comando pondremos free --help. 

Nosotros daremos uso de **free --mega** ya que en el subject aparece esa unidad de medida (Megabyte). 

<aside>
💡 Es importante poner --mega y no -m. Con -m nos referiremos a la unidad de medida Mebibyte y no es la que especifica el subject.

</aside>

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f1d0a5aa-16d1-4ef4-9ff6-489fcb9e0546/Untitled.png)

Para mostrar la memoria usada, usamos el comando 

```bash
**awk**
```

********AWK******** es una herramienta de procesamiento de texto que se utiliza principalmente para manipular datos en formato tabular o de líneas separadas por campos. Aunque puede ser útil para algunas tareas de procesamiento de archivos CSS, no es una herramienta diseñada específicamente para trabajar con hojas de estilo en cascada (CSS).

El comando **`awk`** es una herramienta muy poderosa en sistemas Unix y Linux **utilizada para procesar y manipular datos en archivos de texto**, así como para generar informes y realizar tareas de transformación en la línea de comandos. 

**`awk`** opera en la base de "patrón-acción". Analiza cada línea de un archivo de entrada, compara si cumple con un patrón especificado y, si lo hace, ejecuta la acción correspondiente. Aquí hay un ejemplo simple de su estructura básica:

```arduino
arduinoCopy code
awk 'patrón { acción }' archivo

```

Algunos usos comunes de **`awk`** incluyen:

1. **Extracción de columnas de datos:** Puedes usar **`awk`** para extraer datos específicos de una columna en un archivo de texto. Por ejemplo, para imprimir la segunda columna de un archivo CSV:
    
    ```c
    arduinoCopy code
    awk -F ',' '{ print $2 }' archivo.csv
    
    ```
    
2. **Filtrado y búsqueda:** Puedes usar **`awk`** para filtrar líneas que cumplan con ciertos criterios. Por ejemplo, para imprimir solo las líneas que contienen la palabra "error":
    
    ```c
    cCopy code
    awk '/error/ { print }' archivo.log
    ```
    
3. **Cálculos y agregaciones:** **`awk`** puede realizar cálculos matemáticos y agregar datos. Por ejemplo, para calcular el promedio de una columna numérica:
    
    ```c
    arduinoCopy code
    awk '{ suma += $1; contador++ } END { print suma / contador }' datos.txt
    ```
    
4. **Manipulación y transformación de datos:** Puedes usar **`awk`** para aplicar cambios a los datos, como cambiar el formato de una fecha o realizar reemplazos de texto.
5. **Formateo de informes:** **`awk`** puede formatear y presentar datos de manera legible. Por ejemplo, para imprimir un informe con un formato específico:
    
    ```c
    swiftCopy code
    awk '{ printf "Nombre: %s, Edad: %d\n", $1, $2 }' datos.txt
    ```
    

Estos son solo ejemplos básicos de lo que puedes hacer con **`awk`**. La herramienta es muy versátil y puede ser utilizada para una amplia variedad de tareas relacionadas con el procesamiento y manipulación de datos en archivos de texto en entornos Unix y Linux.

**Comparar:** Por último lo que haremos será comparar si la primera palabra de una fila es igual a "Mem:"  imprimiremos la tercera palabra de esa fila que será la memoria usada. 

```bash
 free --mega | awk '$1 == "Mem:" {print $3}'
```

En el script el valor de retorno de este comando se lo asignaremos a una variable que concatenaremos con otras variables para que todo quede igual como especifica el subject.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/606c205e-16f7-4a11-be85-c74c4e69191c/Untitled.png)

Para obtener la memoria total el comando es practicamente igual al anterior lo único que deberemos cambiar es que en vez de printar la tercera palabra de la fila queremos la segunda:

```bash
 free --mega | awk '$1 == "Mem:" {print $2}'
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d1687e6f-4d84-4726-a2b1-9843c5ff8ec1/Untitled.png)

C**alcular el % de memoria usada**

El comando es parecido a los anteriores, la única modificación que haremos en la parte de la impresión. 

Como la operación para conseguir el porcentaje no es exacta nos puede dar muchos decimales y en el subject solo aparecen 2 de modo que nosotros haremos lo mismo, por eso utilizamos `%.2f` para que asi solo se muestren 2 decimales. 

<aside>
💡 Otra cosa que quizás no sepas es en printf para que se muestre un `%` hay que poner `%%`

</aside>

```bash
free --mega | awk '$1 == "Mem:" {printf("(%.2f%%)\n", $3/$2*100)}'.
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/33c391d0-14a9-4a8c-963b-05306bf1c9de/Untitled.png)

## Memoria del disco

Para ver la memoria del disco ocupada y disponible utilizaremos el comando: **df** 

Este comando significa "disk filesystem", se utiliza para obtener un resumen completo del uso del espacio en disco. 

Como en el subject se indica la memoria utilizada y esta se muestra en MB utilizaremos la flag **-m**

**`-m`**: Es una opción que se utiliza para mostrar los tamaños en megabytes (MB). Si no se especifica esta opción, los tamaños se mostrarán en bloques de 1 kilobyte (KB) por defecto. 

Acto seguido haremos un grep para que solo nos muestre las lineas que contengan "/dev/" y seguidamente volveremos a hacer otro grep con el flag -v para excluir las lineas que contengan "/boot". 

La flag **-v** se usa para Invertir la búsqueda,  para mostrar líneas que no coincidan con el patrón de busqueda.

Por último utilizaremos el comando awk y sumaremos el valor de la tercera palabra de cada linea para una vez sumadas todas las lineas printar el resultado final de la suma

```css
df -m | grep "/dev/" | grep -v "/boot" | awk '{memory_use += $3} END {print memory_use}'
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8b9440b7-bafe-4651-9be7-d306801d730a/Untitled.png)

 

## Espacio total

Para el espacio total se usará un comando muy parecido. Las unicas diferencias seran:

- En este caso sumaremos $2 en vez de $3
- En el subject aparece el tamaño total en Gb como el resultado de la suma nos da el numero en Mb debemos transformarlo a Gb , para ello debemos dividir el numero entre 1024 y quitar los decimales.

```css
df -m | grep "/dev/" | grep -v "/boot" | awk '{use += $3} {total += $2} END {print ("%d%%\n"), use/total*100}
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c161ea27-e423-4489-b00c-9a19d4a45ba2/Untitled.png)

## Porcentaje uso de CPU

Para ver el porcentaje de uso de CPU haremos uso del comando `vmstat`

**`vmstat`** es una herramienta de línea de comandos que se utiliza en sistemas Linux y Unix para proporcionar información sobre el uso de la memoria virtual, el uso de la CPU y la actividad del sistema. Su nombre proviene de "virtual memory statistics" (estadísticas de memoria virtual)

```css
vmstat [opciones] [intervalo] [contador]
```

Donde:

- **`opciones`**: Son argumentos opcionales que permiten personalizar la salida del comando.
- **`intervalo`**: Es el tiempo en segundos entre cada muestra de estadísticas. Si se omite, **`vmstat`** mostrará las estadísticas una vez y luego finalizará.
- **`contador`**: Es el número de muestras que **`vmstat`** mostrará antes de finalizar. Si se omite, **`vmstat`** mostrará estadísticas continuamente hasta que se interrumpa manualmente (por ejemplo, presionando **`Ctrl + C`**).

Para este caso, podríamos no incluir ningun intervalo, sin embargo en la guía se **proponen 1 a 4.** 

Tambien daremos uso del comando `tail -1` 

**********Tail********** para mostrar la última línea de un archivo. En este caso, la opción **`-1`** indica que solo se debe mostrar la última línea del archivo.

De las 4 líneas generadas solo se printara la última. Por ultimo solo printaremos la palabra 15 que es el uso de memoria disponible. 

El comando usado será:

```css
vmstat 1 4 | tail -1 | awk '{print %15}'.
```

El resultado de este comando solo es una parte del resultado final ya que todavia hay que hacer alguna operación en el script para que quede bien.

Para terminar hay que a 100 restarle la cantidad que nos ha devuelto la linea de comandos anterior, el resultado de esa operación imprimimos con un decimal y un % al final y ya estaría hecha la operación.

```css
vmstat 1 3 | tail -1 | awk '{print $15}'.
```

## Ultimo reinicio

Si deseamos ver la fecha y hora de nuestro ùltimo reinicio haremos uso del comando who con el flag -b 

La opción **`-b`** representa "boot time", lo que indica que el comando mostrará la información relacionada con el tiempo de inicio del sistema.

El comando **`who -b`** puede ser útil para verificar cuándo se inició el sistema por última vez, lo que puede ser relevante para el mantenimiento, la solución de problemas o la administración del sistema.

Para filtrar la información presentada, usaremos el comando awk y compararemos si la primera palabra de una linea es "system" así se imprimirá en pantalla la tercera palabra de esa linea , un espacio y la cuarta palabra:

```css
who -b | awk '$1 == "system" {print $3 " " $4}’
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22312980-dc8b-47e7-a954-61e6c50d5f09/Untitled.png)

## ¿Qué son los **LVM?**

**LVM (Logical Volume Manager)** es un sistema de administración de volúmenes lógicos que se utiliza en sistemas operativos tipo Unix. Proporciona una capa de abstracción sobre los discos físicos y permite una gestión más flexible y dinámica del almacenamiento en bloques.

**Con LVM,** los discos físicos se agrupan en grupos de volúmenes (Volume Groups), y luego estos grupos de volúmenes se dividen en volúmenes lógicos (Logical Volumes). 

Los volúmenes lógicos actúan como particiones virtuales y pueden ser formateados y montados como si fueran particiones reales. Lo interesante es que los volúmenes lógicos pueden crecer o reducirse en tamaño de manera dinámica, lo que permite una administración más flexible del espacio de almacenamiento.

### Uso de LVM

Para revisar si LVM esta activo o no haremos uso del comando lsblk. 

**`lsblk`** es una herramienta de línea de comandos en sistemas Linux que se utiliza para listar información sobre los dispositivos de bloque en el sistema, como discos duros, unidades USB, particiones y volúmenes lógicos (LVM).

Se usará el condicional  if ya que se imprimirá un Yes o No. La idea es  contar el numero de lineas en las que aparece "lvm" y si hay mas de 0 se imprimirá **Yes**, si hay 0 se imprimirá **No**. Todo el comando seria: 

```css
if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi.
```

**`$(lsblk | grep "lvm" | wc -l)`**: Esta parte es una secuencia de comandos que se ejecuta entre paréntesis **`$()`**. Realiza una serie de comandos para listar los dispositivos de bloque (lsblk), busca líneas que contengan la cadena "lvm" (grep "lvm") y luego cuenta el número de líneas resultantes (wc -l). En resumen, esto cuenta cuántos dispositivos de bloque contienen "lvm" en su nombre o descripción.

<aside>
💡 El **`fi`** cierra el bloque **`if`**, indicando que los comandos dentro de este bloque se han completado y que el script debe continuar con el resto de las instrucciones.

</aside>

## **Conexiones TCP**

Las conexiones TCP (Transmission Control Protocol) son un tipo de comunicación en redes de computadoras que proporciona una transferencia de datos confiable y orientada a la conexión entre dos dispositivos en una red. TCP es uno de los protocolos más utilizados en Internet y en redes locales, y es parte fundamental del modelo de referencia TCP/IP.

Si queremos consultar la cantidad de conexiones TCP establecidas en el sistema en un momento dado.

```css
ss -ta | grep ESTAB | wc -l
```

En este caso:

**`ss -ta`**: El comando **`ss`** (Socket Statistics) se utiliza para mostrar estadísticas de red. La opción **`-t`** indica que solo se mostrarán conexiones TCP, y la opción **`-a`** muestra todas las conexiones, incluidas las que están establecidas y las que están a la espera de establecerse.

**`|`**: El símbolo de tubería (**`|`**) se utiliza para redirigir la salida del comando anterior (**`ss -ta`**) como entrada para el siguiente comando (**`grep ESTAB`**).

**`grep ESTAB`**: El comando **`grep`** se utiliza para buscar líneas que contengan la palabra "ESTAB" (que es el estado para conexiones TCP establecidas). En otras palabras, filtra solo las líneas que muestran conexiones TCP que están en estado establecido.

**`wc -l`**: El comando **`wc`** (Word Count) se utiliza para contar líneas, palabras y caracteres. La opción **`-l`** le indica a **`wc`** que solo cuente las líneas. Por lo tanto, este comando cuenta la cantidad de líneas que coinciden con "ESTAB", lo que representa la cantidad de conexiones TCP establecidas.

## Número de usuarios

Daremos uso del comando `users` que nos mostrará el nombre de los usuarios que hay, sabiendo esto, pondremos wc -w para que cuente la cantidad de palabras que hay en la salida del comando. 

El comando entero queda así `users | wc -w`.

## Dirección IP- MAC

Para obtener la dirección del host haremos uso del comando 

```css
hostname -I 
```

y para obtener la MAC haremos uso del comando:

```css
ip link 
```

Este comando se utiliza para mostrar o modificar las interfaces de red. 

Como aparece más de una interfaz, IP's etc. Utilizaremos el comando grep para buscar lo que deseamos y asi poder imprimir por pantalla solo lo que nos piden. 

```css
ip link | grep "link/ether" | awk '{print $2}' 
```

## **Número de comandos ejecutados con sudo**

Para poder obtener el numero de comandos que son ejecutados con sudo haremos uso del comando jornalctl 

El comando **`journalctl`** es una herramienta de línea de comandos utilizada en sistemas Linux que permite acceder y leer el registro del sistema, conocido como el "systemd journal" o "journal de systemd". 

El journal de systemd es un sistema de registro centralizado que almacena información detallada sobre eventos y mensajes del sistema, como mensajes de arranque, cierre, errores, advertencias y otros registros del kernel y servicios del sistema.

Acto seguido pondremos `_COMM=sudo` para así filtrar las entradas especificando su ruta. 

_COMM=sudo, es el filtro que busca procesos o registros que estén ejecutando el comando **`sudo`**.

Una vez tengamos filtrada la busqueda y solo aparezcan los registros de sudo todavía  deberemos filtrar un poco más ya que cuando incias o cierras sesion de root tambien aparece en el registro, entonces para terminar de filtrar pondremos un `grep COMMAND` y asi solo apareceran las lineas de comandos. 

Por ultimo pondremos `wc -l` para que asi nos salgan enumeradas las lineas. El comando entero es el siguiente:

```css
 journalctl _COMM=sudo | grep COMMAND | wc -l)
```

Para comprobar que funcione correctamente podemos correr el comando en el terminal, poner un comando que incluya sudo y volver a correr el comando y deberá incrementar el número de ejecucciones de sudo.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc7d3c1a-501c-4848-9330-1249c4ebe0ff/Untitled.png)

# Crontab

Crontab (Tabla de Cron) es un archivo en sistemas Unix y Linux que contiene una lista de comandos que se ejecutan automáticamente a intervalos de tiempo específicos. Estos comandos programados se conocen como "tareas cron" o simplemente "cron jobs". Crontab permite automatizar tareas repetitivas o programar la ejecución de scripts y comandos en momentos específicos, lo que es especialmente útil para tareas de administración y mantenimiento del sistema.

Para tener correctamente crontab configurado debemos editar el fichero crontab con el siguiente comando:

```css
sudo crontab -u root -e
```

En el fichero debemos añadir el siguiente comando para que el script se ejecute cada 10 minutos

```css
*/10 * * * * sh /ruta del script.
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/aa76117f-ca2e-43bd-b5c9-07ec40225cbc/Untitled.png)

Funcionamiento de cada parametro de crontab:

- m ➤ Corresponde al minuto en que se va a ejecutar el script, el valor va de 0 a 59.
- H ➤ La hora exacta, se maneja el formato de 24 horas, los valores van de 0 a 23, siendo 0 las 12:00 de la medianoche. dom ➤ hace referencia al día del mes, por ejemplo se puede especificar 15 si se quiere ejecutar cada dia 15.
- **Dow** ➤ Significa el día de la semana, puede ser numérico (0 a 7, donde 0 y 7 son domingo) o las 3 primeras letras del día en inglés: mon, tue, wed, thu, fri, sat, sun.
- **user** ➤ Define el usuario que va a ejecutar el comando, puede ser root, u otro usuario diferente siempre y cuando tenga permisos de ejecución del script.
- **Command** ➤ Refiere al comando o a la ruta absoluta del script a ejecutar.

# Signature.txt

Para obtener la firma lo primero que debemos hacer es apagar la máquina virtual ya que una vez la enciendas o modifiques algo la firma cambiará.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/639054a9-04c3-4f68-92b5-9c04cf8a2b43/Untitled.png)

El siguiente paso será ubicarnos en la ruta donde tengamos el .vdi de nuestra maquina virtual.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/745d0d16-852a-4ea6-b979-754b487cc5cc/Untitled.png)

Por último haremos `shasum nombremaquina.vdi` y esto nos dara la firma. 

**El resultado de esta firma es lo que tendremos añadir a nuestro fichero signature.txt para posteriormente subir el fichero al repositorio de la intra.**

Muy importante no volver a abrir la maquina ya que se modificara la firma. 

Para las correcciones recuerda clonar la maquina ya que asi podras encenderla sin miedo a que cambie la firma.

## ¿Qué es shasum?

Es una herramienta de línea de comandos utilizada en sistemas Unix y Linux para calcular el valor de resumen (hash) de un archivo o entrada de datos. El valor de resumen, también conocido como hash, es una cadena alfanumérica única que representa los datos en su totalidad. Si los datos cambian, incluso por un solo bit, el valor de resumen también cambiará significativamente.

Los hashes tienen muchas aplicaciones útiles en la informática, algunas de las cuales son:

- Almacenamiento seguro de contraseñas: En lugar de almacenar las contraseñas de manera directa, los sistemas suelen almacenar sus valores de resumen, lo que evita que las contraseñas se revelen fácilmente en caso de una violación de seguridad.
- Tablas hash: Se utilizan para implementar estructuras de datos como tablas hash, que permiten una búsqueda y acceso rápido a datos en función de una clave.
- Verificación de integridad de datos: Los hashes se utilizan para verificar si los datos se han corrompido o han cambiado durante la transferencia o el almacenamiento, al comparar los valores de resumen antes y después del proceso.
- Firma digital: Las firmas digitales se generan mediante funciones de hash para garantizar la autenticidad e integridad de un mensaje o archivo.

```css
shasum [opciones] archivo
```

En sistemas macOS, el comando **`shasum`** se utiliza para calcular el SHA-1 (Secure Hash Algorithm 1) de un archivo o entrada de datos. SHA-1 es un algoritmo de hash criptográfico ampliamente utilizado, pero se considera inseguro para aplicaciones criptográficas debido a sus vulnerabilidades

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/247d1a4b-c7f2-4ecb-a18f-52071536edd3/Untitled.png)

# Tipos de particiones

- **Primaria:** La única partición en la que puede estar instalada un SO. Solo pueden haber 4 particiones primarias por disco duro o 3 primarias y una extendida.
- **Secundario/Extendida:** Fue ideada para romper la limitación de 4 particiones primarias en un solo disco físico. Solo puede existir una partición de este tipo por disco, y solo sirve para contener particiones lógicas.
- **Lógica:** Ocupa una porción de la partición extendida/primaria o la totalidad de la misma, la cual se ha formateado con un tipo específico de sistema de archivos (en nuestro caso usaremos ext4) y se le ha asignado una unidad, así el sistema operativo reconoce las particiones lógicas o su sistema de archivos. Puede haber un máximo de 23 particiones lógicas en una partición extendida , sin embargo linux el SO con el que trabajamos actualmente lo reduce a 15, más que suficientes para realizar este proyecto.

# Lighttpd

Es un servidor web ligero y de código abierto que fue diseñado para ser rápido, eficiente y de bajo consumo de recursos. Es una alternativa a otros servidores web populares como Apache y Nginx, y se ha ganado una reputación por su excelente rendimiento y facilidad de configuración.

Algunas características y ventajas clave de Lighttpd son:

1. Ligero y eficiente: Lighttpd está diseñado para ser ligero y consume menos recursos en comparación con otros servidores web, lo que lo hace ideal para servidores con recursos limitados o para manejar altas cargas de tráfico.
2. Alto rendimiento: Lighttpd está optimizado para manejar solicitudes web de manera eficiente y rápida, lo que lo convierte en una excelente opción para aplicaciones que requieren alta velocidad de respuesta y bajo tiempo de latencia.
3. Configuración sencilla: Su configuración se realiza mediante un archivo de configuración simple y fácil de entender, lo que facilita su puesta en marcha y administración.
4. Admite múltiples módulos: Lighttpd es extensible a través de módulos que proporcionan funcionalidades adicionales, como soporte para PHP, SSL, FastCGI, entre otros.
5. Implementa FastCGI y SCGI: Lighttpd es compatible con los protocolos FastCGI y SCGI, lo que permite ejecutar aplicaciones web escritas en diferentes lenguajes de programación, como PHP, Python y Ruby.
6. Soporte para compresión: Lighttpd tiene soporte integrado para la compresión Gzip, lo que permite comprimir el contenido antes de enviarlo al cliente, lo que mejora la velocidad de carga de la página.
