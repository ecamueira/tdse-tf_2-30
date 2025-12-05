

 <img src="https://github.com/user-attachments/assets/15600b18-f73b-4ba3-a959-47f0048a1ab6" alt="image2" width="50%">


# **Sistema Automático de Gestión de Cultivos (SAGC)**

 

**Autores: Camueira Elias; Cascia Serena; Donadello Nicolas**

**Padrón: 110772; 107946;112007**

**Fecha: 2do cuatrimestre 2025**

 

 

 

 

### **1\. Selección del proyecto a implementar**

#### **1.1 Objetivo del proyecto y resultados esperados**

El objetivo de este proyecto es desarrollar un sistema automatizado de cultivo que permita medir, registrar y controlar variables ambientales críticas (temperatura, humedad, riego, fertilización) e implementar iluminación espectral controlada (incluyendo rojo, azul y UV-A) para favorecer el desarrollo óptimo de los cultivos en sus distintas etapas.Además, a través de una aplicación móvil, el usuario puede cargar datos sobre el progreso del cultivo y ajustar parámetros. El sistema utiliza esta información para refinar su respuesta y optimizar el control de acuerdo con las necesidades específicas del cultivo.

#### **1.2 Proyectos similares**

En base al objetivo se proponen posibles proyectos que requieren el uso de hardware específico y se ponderan los aspectos a tener en cuenta para seleccionar el más adecuado.

1. Base: Control con monitoreo de humedad del suelo y temperatura y humedad del aire con irrigación de agua y fertilizantes e iluminación personalizada.
2. Base + medidor de pH: Control con monitoreo de humedad del suelo, temperatura y humedad del aire y calidad de los suelos (Índice de pH) con irrigación de agua y fertilizantes e iluminación personalizada.
3. Base + medidor de caudal: Control con monitoreo de humedad del suelo y temperatura y humedad del aire con irrigación (finamente monitoreada a través de un caudalímetro) de agua y fertilizantes e iluminación personalizada.

Para comparar estas alternativas, se tienen en cuenta seis aspectos característicos, los cuales se ponderan del 1 al 10:
1.  **Disponibilidad del hardware (9):** Se evalúa si el proyecto puede implementarse utilizando hardware que se consiga fácilmente en el mercado regional, sin necesidad de importación o tiempos de envío extensos.
2.  **Impacto en el proyecto (8):** Se pondera cuánto aporta a la funcionalidad y control del crecimiento del cultivo.
3.  **Costo (8):** Se evalúa el costo total del hardware requerido para cada opción.
4.  **Dificultad técnica / Viabilidad (10):** Se contempla el tiempo requerido y la complejidad de implementación, teniendo en cuenta los conocimientos disponibles.
5.  **Interés personal del equipo (7):** Se pondera la motivación e interés del equipo en implementar cada alternativa.

La siguiente tabla (Tabla 1.2.1) muestra los valores ponderados asignados a cada proyecto considerado

<table>
        <thead>
            <tr>
                <th rowspan="2">Proyecto</th>
                <th colspan="2">Base</th>
                <th colspan="2">Base + medidor de pH</th>
                <th colspan="2">Base + medidor de caudal</th>
            </tr>
            <tr>
                <th>Puntaje</th>
                <th>Puntaje Ponderado</th>
                <th>Puntaje</th>
                <th>Puntaje Ponderado</th>
                <th>Puntaje</th>
                <th>Puntaje Ponderado</th>
            </tr>
        </thead>
        <tbody>
            <tr class="header-row">
                <td align ="center">Disponibilidad de Hardware <br>(peso : 10)</td>
                <td>10</td>
                <td>100</td>
                <td>10</td>
                <td>100</td>
                <td>4</td>
                <td>40</td>
            </tr>
            <tr>
                <td align ="center">Facilidad de Acceso <br>(peso : 8)</td>
                <td>8</td>
                <td>64</td>
                <td>5</td>
                <td>40</td>
                <td>10</td>
                <td>80</td>
            </tr>
            <tr class="header-row">
                <td align ="center">Seguridad <br>(peso : 6)</td>
                <td>8</td>
                <td>48</td>
                <td>8</td>
                <td>48</td>
                <td>6</td>
                <td>36</td>
            </tr>
            <tr>
                <td align ="center">Tiempo de Implementación <br>(peso : 8)</td>
                <td>8</td>
                <td>64</td>
                <td>10</td>
                <td>80</td>
                <td>2</td>
                <td>16</td>
            </tr>
            <tr class="header-row">
                <td align ="center">Costo (peso : 5)</td>
                <td>8</td>
                <td>40</td>
                <td>8</td>
                <td>40</td>
                <td>6</td>
                <td>30</td>
            </tr>
            <tr>
                <td align ="center">Interés personal <br>(peso : 8)</td>
                <td>10</td>
                <td>80</td>
                <td>4</td>
                <td>40</td>
                <td>10</td>
                <td>80</td>
            </tr>
            <tr class="highlight-green">
                <td>Puntaje Total</td>
                <td>-</td>
                <td>396</td>
                <td>-</td>
                <td class="highlight-red">348</td>
                <td>-</td>
                <td>282</td>
            </tr>
        </tbody>
</table>
<p align="center"><em>Tabla 1.2.1: Comparación de proyectos</em></p>

#### **1.3 Selección de proyecto**

Considerando la Tabla 1.2.1,  se elige implementar el sistema de acceso con RFID y keypad. El sistema de acceso mediante reconocimiento facial requiere mucho tiempo de implementación y conceptos avanzados de machine learning, lo cual excedería el margen de tiempo que se propone para el proyecto. Adicionalmente, es el más costoso de implementar debido a los requerimientos de una  buena camara con alta definición para poder entrenar la red neuronal con poco ruido. Sufre además de posibles brechas de seguridad intrínseca, dado que la red neuronal puede erróneamente habilitar el acceso a alguien que tiene características faciales similares. Por otro lado, el sistema de acceso mediante únicamente keypad no tiene tanta facilidad de acceso al edificio como el que tiene keypad y RFID, ya que los tags RFID son más rápidos.

Debido a las razones mencionadas anteriormente y a la tabla basada en dichas razones, el proyecto a implementar es un sistema de acceso con una cerradura inteligente que cuenta con un lector RFID y un teclado. La combinación de estos dos sistemas brinda flexibilidad y facilidad de acceso a los usuarios, preservando los estándares de seguridad.

En Argentina, la necesidad de seguridad en hogares y pequeñas empresas motiva la creación de soluciones tecnológicas que no solo sean confiables, sino también accesibles y fáciles de usar. Este proyecto busca una alternativa moderna a las cerraduras tradicionales, brindando flexibilidad y  seguridad simultáneamente. El presente proyecto se destaca especialmente por incorporar un módulo Wi-Fi que permite configurar los permisos de acceso de los individuos y un parlante y micrófono. Esto lo diferencia de otros sistemas similares en que permite seleccionar de forma remota los permisos de acceso y visualizar los intentos de acceso de forma remota. Adicionalmente, permite hablar con el individuo a través de los parlantes y micrófonos cuando no puede acceder a la propiedad. Una última característica especial es la presencia de un sensor magnético, el cual indica cuando se deja abierta la puerta accidentalmente.

Los desafíos principales de este proyecto son la integración de las diferentes tecnologías (RFID, teclado matricial, parlante…), la garantía de seguridad de los datos (encriptación para proteger la información), la optimización energética y el eficiente uso de recursos.

###### **1.3.1 Diagrama en bloques**

En la Figura 1.3.1 se muestra el diagrama en bloques del sistema con los principales módulos del proyecto

<p align="center">
  <img src="https://github.com/user-attachments/assets/57fad928-0021-4330-bb8f-daf010a19ebe" alt="image1">
</p>

<p align="center"><em>Figura 1.3.1: Diagrama en bloques del sistema</em></p>


### **2\. Elicitación de requisitos y casos de uso**

En Argentina existen varios productos de características similares a las del proyecto, cada producto diferenciándose de otro con detalles, como por ejemplo huellas digitales, llaves, etc. Sin embargo, parecería que no hay un producto en Argentina que cumpla exactamente la misma función que el proyecto desarrollado.

Como primer competidor del mercado se puede mencionar a [Yale](https://yalehome.com.ar/categoria-producto/cerraduras-digitales/), la cual ofrece una amplia gama de cerraduras digitales inteligentes para seguridad del hogar. Los precios de sus productos orbitan desde los 45.000 hasta los 600.000 pesos y sus productos incluyen desde cerraduras con teclado matricial hasta cerraduras con huellas digitales, todas con una aplicación para el celular. El proyecto tiene similitudes en el teclado matricial y en la aplicación, pero se diferencia en la oferta de los sensores magnéticos, del lector RFID y de la comunicación con parlante y micrófono.

Un segundo competidor es [Philips](https://www.tienda.philips.com.ar/productos-para-el-hogar/smart-lock/cerraduras-inteligentes), la cual tiene productos con reconocimiento facial y video portero. Esta tecnología es considerablemente superior al igual que sus precios, los cuales rondan el 1.000.000 de pesos. Sin embargo, la empresa no cuenta con lectores RFID ni sensores magnéticos, lo cual diferencia a nuestro proyecto.

En resumen, el mercado es sumamente competitivo y las características y funcionalidades de la cerradura pueden ser modificadas y ampliadas fácilmente, permitiendo desarrollar productos únicos y distintos de la competencia que encuentren un lugar en el mercado.

| Grupo | ID | Descripción |
| :---- | :---- | :---- |
| Acceso | 1.1 | El sistema permitirá el acceso a la instalación mediante RFID |
|  | 1.2 | El sistema permitirá el acceso a la instalación mediante un teclado matricial |
|  | 1.3 | En caso de acceso permitido, el  sistema abrirá la puerta durante un periodo de tiempo fijado |
| Indicadores | 2.1 | El sistema contará con un indicador luminoso para indicar que la puerta está cerrada |
|  | 2.2 | El sistema contará con un indicador luminoso para indicar que la puerta está abierta |
|  | 2.3 | El sistema contará con un parlante que indique mediante sonido cuando se abre la puerta |
|  | 2.4 | El sistema contará con un parlante que indique mediante sonido cuando se introduce un código incorrecto |
|  | 2.5 | El sistema contará con un parlante que indique mediante sonido cuando se presiona una tecla |
|  | 2.6 | El sistema notificará con el parlante cuando se deja la puerta abierta |
|  | 2.7 | El sistema notificará mediante el titileo de leds cuando la puerta se deja abierta o cuando se introduce un código/RFID erróneo |
|  | 2.8 | El sistema notifica con audio y luz cuando se deja un código sin introducir completamente |
| Motor | 3.1  | El sistema contará con un motor para abrir y cerrar la cerradura |
|  | 3.2 | El sistema solo podrá cerrar la puerta cuando esta se halla contra el marco |
| Comunicación Audio  | 4.1 | El sistema deberá contar con un parlante para transmitir señales de audio |
|  | 4.2 | El sistema deberá contar con un micrófono para recibir señales de audio |
| Comunicación Wi-Fi | 5.1 | El sistema se comunicará mediante Wi-Fi con la aplicación de celular |
|  | 5.2 | El sistema deberá enviar a la aplicación la información de acceso a la instalación |
|  | 5.3 | El sistema deberá enviar a la aplicación la información de acceso denegado a la instalación |
|  | 5.4 | En caso de lectura RFID, el sistema deberá comunicar la lectura de RFIDs desconocidos, junto con su ID (para poder guardarlo posteriormente) |
|  | 5.4 | El sistema deberá comunicarle a la aplicación el estado de la puerta y el numero de puerta |
|  | 5.5 | El sistema deberá poder recibir señales de audio de la aplicación |
|  | 5.6 | El sistema deberá poder transmitir señales de audio a la aplicación |
| Aplicación | 6.1 | La aplicación tendrá la base de datos de los individuos habilitados con sus IDs |
|  | 6.2 | La aplicación deberá permitirle al usuario configurar los permisos de acceso de los individuos |
|  | 6.3 | La aplicación deberá poder mostrar la información de los accesos e intentos de acceso |
|  | 6.4 | La aplicación deberá poder controlar manualmente la apertura o cerradura de la puerta |
|  | 6.5 | La aplicación deberá permitirle al usuario configurar añadir nuevos individuos a la base de datos mediante codigo o RFID |
|  | 6.6 | La aplicación deberá mostrarle al usuario el estado de la puerta |
| Interruptores/ Botones | 7.1 | El sistema contará con botones para abrir o cerrar la puerta de forma manual |
|  | 7.2 | El sistema contará con un botón de timbre |
| Sensores | 8.1 | El sistema contará con un sensor magnético que detectará cuando la puerta se halla contra el marco |

<p align="center"><em>Tabla 2.1: Requisitos del proyecto</em></p>

En las tablas 2.2 a 2.4 se presentan 3 casos de uso para el sistema.

| Elemento | Definición |
| :---- | :---- |
| Disparador | Se quiere acceder a la instalación con permiso de acceso y con código en el teclado matricial. |
| Precondiciones | El sistema está encendido La puerta está cerrada, con la  cerradura cerrada. La aplicación está conectada al sistema. El indicador de puerta cerrada está encendido  |
| Flujo principal | El individuo introduce su código en el teclado matricial. Por cada tecla que presione recibe una melodía indicando la recepción del carácter introducido. Una vez introducido todo el código, el motor abre la cerradura y se notifica con una melodía el acceso habilitado. Además, con un led se notifica la habilitación del acceso. El módulo Wi-Fi comunica a la aplicación el acceso a la instalación, mostrando el estado de la puerta, la identificación del ingresante, la hora y el número de puerta. El individuo cierra la puerta una vez adentro. |
| Flujos alternativos | a. El individuo introduce erróneamente el código, con lo cual se notifica auditiva y visualmente al usuario y se notifica mediante Wi-Fi que se intentó acceder sin permiso a la instalación.  b. El individuo deja de introducir el código a mitad de camino. Luego de un tiempo preestablecido, el código a medias se descarta y se notifica que el intento fue incorrecto tanto al individuo como al propietario mediante Wi-Fi.. c. El individuo olvida la puerta abierta, entonces se suena una “alarma” y se notifica al propietario mediante Wi-Fi d. Un usuario dentro de la instalación presiona el botón de cerrar la puerta antes de que se introduzca el código. La puerta permanece cerrada. e. El usuario acerca su tarjeta en vez de terminar el código. La puerta se abre y se indica que la puerta está abierta. |

<p align="center"><em>Tabla 2.2: Caso de uso 1: El usuario quiere acceder con código</em></p>


| Elemento | Definición |
| :---- | :---- |
| Disparador | Se quiere acceder a la instalación con permiso de acceso y con RFID. |
| Precondiciones | El sistema está encendido La puerta está cerrada, con la  cerradura cerrada. La aplicación está conectada al sistema. El indicador de puerta cerrada está encendido  |
| Flujo principal | El individuo acerca su tarjeta al lector. El ID de la tarjeta es correcto, el motor abre la cerradura y se notifica con una melodía el acceso habilitado. Además, con un led se notifica la habilitación del acceso. El módulo Wi-Fi comunica a la aplicación el acceso a la instalación, mostrando el estado de la puerta, la identificación del ingresante, la hora y el número de puerta. El individuo cierra la puerta una vez adentro. |
| Flujos alternativos | a. El individuo usa una tarjeta no habilitada, con lo cual se notifica auditiva y visualmente al usuario y se notifica mediante Wi-Fi que se intentó acceder sin permiso a la instalación.  b. El individuo olvida la puerta abierta, entonces se suena una “alarma” y se notifica al propietario mediante Wi-Fi |

<p align="center"><em>Tabla 2.3: Caso de uso 2: El usuario quiere acceder con RFID</em></p>


| Elemento | Definición |
| :---- | :---- |
| Disparador | Se quiere añadir una nueva tarjeta RFID |
| Precondiciones | El sistema está encendido La puerta está cerrada, con la  cerradura cerrada. La aplicación está conectada al sistema. El indicador de puerta cerrada está encendido |
| Flujo principal | Se acerca una tarjeta desconocida al lector RFID. El sistema indica que el intento de acceso es incorrecto. El sistema muestra el ID de la tarjeta e indica si se quiere guardar la tarjeta mediante comunicación Wi-Fi con la aplicación. |
| Flujos alternativos | a. Se pierde la conexión Wi-Fi. El sistema no puede continuar con el guardado de la tarjeta. Se indica que se perdió la conexión b. Se apaga el sistema. El sistema no puede continuar con el guardado de la tarjeta.  |

<p align="center"><em>Tabla 2.4: Caso de uso 3: El usuario quiere guardar una tarjeta RFID</em></p>
