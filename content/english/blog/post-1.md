---
date: "2022-03-02T10:07:21+06:00"
description: This is meta description
draft: false
image: images/blog/post-1.jpg
title: I. Estadística descriptiva y Análisis exploratorio.  
type: featured
---

### Sesión 2

#### Objetivo 

Presentar la vinculación entre estadística descriptiva e inferencial, así como implementar el cálculo de los estimadores clásicos usando el lenguaje R la plataforma R Studio. Y el lenguaje Python mediante la aplicación Jupyter Notebooks. 

##### Objetivos específicos. 

+  El alumno aprenderá la importancia de la realización de análisis  replicable de datos. ¿Qué entendemos por análisis estadistico replicable?

+ El alumno conocerá las herramientas para trabajar en un entorno replicable de análisis estadístico. Concretamente se presentarán las herramientes de código abierto **R Studio** y  **Jupyter notebooks** basadas en el lenguaje R y **Python** respectivamente.

+ El alumno será capaz de realizar estimaciones  y en su caso representar visualmente, la  distribución de frecuencia, las medidas de tendencia central y dispersión (Media, Mediana, Moda. Rango).

##### Tiempo asignado para el tema:
3 horas. 


### Actividad a evaluar.
Estimación de medidas de tendencia central y  visualización. 





> ### Software Setup (Installation).

![](/images/blog/r.jpg)


1. On wndows: [download](http://cran.cnr.berkeley.edu/)
2. Mac [download](http://cran.cnr.berkeley.edu/)

R studio 

3. Windows and Mac [download](https://www.rstudio.com/products/rstudio/download/#download)

![](/images/blog/installrstudio.jpg) 




### Algunas consideraciones preeliminares sobre R.

## IDE 

R es un lenguaje que nos permite hablar con la computadora, wn analogía con cualquier lenguaje, como aprenderemos existen **sustantivos**, estos son los objetos (data frames o conjunto de adtos),  las funciones pueden entenderse como **verbos** y sus argumentos como **adverbios**.

Estamos aprendiendo un lenguaje para comunicarnos con nuestra computadora con la finalidad de conducir tareas de análisis de datos. 

En la base del proceso de análisis de datos se encuentra la habilidad para almacenar **grandes cantidades de datos** y tener la capacidad para sustraer estos datos cuando lo necesitamos. 

El resto  de actividades como la **manipulación de los datos**, su **visualización** y el **modelado** son etapas en la secuencia del proceso de análisis. 


## IDE Componentes del entorno de trabajo en R  Studio

El entono de trabajo de **R**, (IDE *Integrated Development Environment*) permite introducción de  código para ejecutar estimaciones. Cuatro secciones principales para trabajo: 



![](/IDE.jpg)

![](/IDE2.jpg)


 **Source pane** Permite el registro de los comandos las operaciones utilizadas. (el código utilizado)
 
![](/source.jpg)

**Environment** 

![](/environment.jpg)

**Console y Terminal pane** Area para  introducir código y  ejecutarlo.

![](/console.jpg)

**Viewer**


![](/viewer.jpg)


A medida que avanzamos con el aprendizaje de la implementación en R aprenderemos a manejar elementos en el entorno de R como: **los objetos**, **tipos de datos**,  **notación**, **funciones**, etc.,

### Instalación de Paquetes.

Estos se integran por  funciones que se han construido por miembros de la comunidad, nos permiten realizar operaciones concretas así como estimar procedimientos estadisticos de diverso gado de complejidad.
Para poder utilizar estos paquetes es necesario instalarlos y activarlos en el espacio de trabajo usando el menú Install y Packages. Área inferior izquierda. La siguiente figura muestra el menú para instalarlos.


![](/Packages.jpg)


Alternativamente podemos utilizar la línea de comandos para hacer la instalación usando la función: `install.packages("ggplot2")`.

Un paquete básico es `tidyverse` este es una colección de funciones y es útil para realizar  tareas de análisis de datos e incluye herramientas  para visualización como `ggplot`. 

Una vez que tenemos el paquete que necesitamos instalado, lo activamos con la función  `library()`.


Una via básica de consulta para conocer los propósiots y los paramétros necesarios para las diferentes funciones para anáisis,  es la documentación de ayuda. Esto se hace anteponiendo un signo $?$  al nombre de la función.   Ej. `?mutate`. *IMPORTANTE*, la libreria que contiene la funcion debe estar actualmente activa para poder acceder a la documentación solicitada. 


### Consideraciones a recordar sobre los tipos de variables  clases y tipo de atributos.

- Numeric

- Strings 

- Factors

Esta clase se permite almacenar información categórica,  datos que son categóricos por ejemeplo los estados de la república mexicana, sabemos que son 32 y pueden ser almacenados como un vector de factores, en una variable categórica. 

El vector sexo con valores c("Mujer","Hombre"), igual es de clase factor. Un conjunto de rangos de edad por ejemplo con factores en un vector como grupo_e<-C(1,2,3,4)  para 1:0-12 años, 2:13-24, 3:25-34 y 4 35-64 años. 

Estas variables se pueden representar con vectores de clase factor. Esencialmente un factor es una categoría. Note que  no son variables cuyo orden o magnitud sea de terminante. Por ejemplo en el vector sexo  el 2: Mujer,  no es más que uno: Hombre. 

Para asignar la clase **factor** a un vector únicamente pasamos la funcion `as.factor()`   del paquete `tidyverse` o bien la *built in* función   `factor()`. R almacenará los datos en un vector de enteros **integer** . R también agregará el atributo **levels** al atributo ya existente **class**.

