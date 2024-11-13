# Adquisición máquina comprometida basada en la metodología (Pasos 1-3)

## 1. Preparación
Para realizar la adquisición de la máquina comprometida hay que comenzar preparando las herramientas que se van a utilizar en el proceso. Para ello, prepararía un USB si fuera un sistema normal, en este caso al ser una máquina virtual y no poder instalar nada externo he creado un disco virtual con las herramientas que me ayudarán a adquirir los datos del sistema. En mi caso voy a utilizar las siguientes herramientas:
+ **RAM Capturer**: Herramienta encargada de realizar la adquisición de RAM.
+ **IRTriage**: Herramienta encargada de realizar el triage.
+ **FTK Imager**: Herramienta encargada de realizar la adquisición de disco y como segunda opción para la RAM.

![Herramientas del USB](/pictures/herramientasDisco.png)

## 2. Adquisición
Para realizar la adquisición comenzaré obteniendo la información de la **RAM** ya que su memoria es volátil y esta, puede tener información que no se encuentra en el disco.
Al llegar al equipo comprometido lo he encontrado de la siguiente manera:

![Pantalla inicio](/pictures/pantallaInicio.png)

Comenzaré utilizando la herramienta **Ram Capturer** como he mencionado en el apartado anterior. Para utilizar la herramienta solo tendremos que ejecutar la herramienta y pulsar sobre *Capture* habiendo especiifcado antes la ruta en la que guardar el archivo obtenido.

![Ram capturer](/pictures/ramCapturer.png)

Una vez obtenida la información de la RAM, voy a realizar el **triage** para recoger algunos archivos que pueden ser bastante importantes a la hora de concluir qué es lo que ha ocurrido en el equipo.
Para realizar el triage voy a utilizar la herramienta IRTriage, la cual para utilizarla solo hay que ejecutarla, rellenar los datos que solicita y elegir los archivos que se quieren obtener, que en mi caso he elegido todos los que nos ofrece la herramienta.

![IRTriage datos](/pictures/IRTriage.png)

![IRTriage archivos seleccionados](/pictures/IRTriage2.png)

Finalmente voy a proceder a la adquisición del disco, para ello utilizaré la herramienta **FTK Imager**.

![Foto FTK Imager](/pictures/FTKImager.png)

Con esta herramienta lo que voy a crear es una **imágen lógica** del disco. A continuación debo rellenar los datos del caso.

![Foto datos del caso](/pictures/FTKImager2.png)

Una vez realizada la adquisición del disco, la herramienta devuelve el **HASH en MD5 y en SHA1** como se puede observar en la imagen.

![Foto adquisición finalizada](/pictures/FTKImager3.png)

### Acta de adquisición

| Acta de Adquisición Forense |  |
| --- | --- |
| Fecha y hora | 13/11/2024   12:08 |
| Lugar | C/Amiel, s/n |
| Perito forense | Lucía Espinosa Sánchez |
| Solicitante | Manuel Rivas |
| **Descripción del dispositivo** |  |
| Tipo de dispositivo | Ordenador |
| Marca y modelo | MSI Thin GF63 |
| Número de serie | —- |
| Capacidad | 32GB  1GB RAM |
| Estado físico | Aparentemente normal, sin defectos |
| **Procedimiento de adquisición** |  |
| Método de adquisición | Imagen lógica, volcado de RAM y triage |
| Herramientas utilizadas | RAM Capturer, FTK Imager, IR Triage |
| Configuración | Sin configuración previa |
| **Integridad de la evidencia** |  |
| Valor hash original | F80726D08B3CF346B75DD563ED4270B3A22B79E7 |
| Algoritmo utilizado | MD5, SHA-1 |
| Valor hash de la copia RAM SHA1 | F80726D08B3CF346B75DD563ED4270B3A22B79E7 |
| Valor hash de la copia RAM MD5 | 09C345378ADB66FE8805654EDC343C57 |
| Valor hash de la copia Triage SHA1 | C4CD2FFAE9564E2796CFF54841DA45105A564CC0 |
| Valor hash de la copia Triage MD5 | 8D684B9540E0C672F4E4F60A2C845B21 |
| Valor hash de la copia Disco SHA1 | A9D360C3B17D9DAA07BCE256DC9AABAB63CA6340 |
| Valor hash de la copia Disco MD5 | 6B7E38922A49A033370F219FDAD0A20D |
| **Observaciones** |  |
| **Firmas** |  |
| Perito forense | Lucía Espinosa Sánchez |
| Testigo | —- |
| Responsable | Lucía Espinosa Sánchez |

## 3. Preservación

Las evidencias están guardadas en diversos sitios para tener varias copias por si hubiera algún error con alguna de ellas. Una de las copias de las evidencias se encuentran en un USB y en mi ordenador. Además, estas evidencias están subidas a una carpeta [Drive](https://drive.google.com/drive/folders/1CWaoP_wDCJ662R02Kv-MWTBTNg69CYca?usp=sharing) donde podrá revisarlas.

### Cadena de custodia

| Tipo de evidencia | Fecha y hora de recolección | Recolectado por | Hash de la evidencia | Método de adquisición | Estado de la evidencia |
| --- | --- | --- | --- | --- | --- |
| Disco duro (C:) | 13/11/2024  19:35 | Lucía Espinosa Sánchez | SHA1-A9D360C3B17D9DAA07BCE256DC9AABAB63CA6340  MD5-6B7E38922A49A033370F219FDAD0A20D | Imágen lógica | En formato digital en una carpeta en Drive |
| Memoria RAM | 13/11/2024  12:08 | Lucía Espinosa Sánchez | SHA1-F80726D08B3CF346B75DD563ED4270B3A22B79E7  MD5-09C345378ADB66FE8805654EDC343C57 | Volcado de Ram | En formato digital en una carpeta en Drive |
| Archivos del sistema | 13/11/2024  18:36 | Lucía Espinosa Sánchez | SHA1-C4CD2FFAE9564E2796CFF54841DA45105A564CC0  MD5-8D684B9540E0C672F4E4F60A2C845B21 | Triage | En formato digital en una carpeta en Drive |