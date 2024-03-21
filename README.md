
<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Danmunozbe/Practica1/tree/Pain2">
    <img src="Recursos/UNAL.png" alt="Logo">
  </a>

  <h3 align="center">Laboratorio 1: Diseño de logotipo en tablero</h3>

  <p align="center">Robótica
    <br />
    <a href="https://github.com/Danmunozbe/Practica1/tree/Pain2"></a>
    <br />Daniel Muñoz · Christian Vargas
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Índice</summary>
  <ol>
    <li>
      <a href="#Planteamiento del problema">Planteamiento del problema</a>
    </li>
    <li>
      <a href="#Desarrollo">Desarrollo</a>
      <ul>
        <li><a href="#Diseño del logo">Diseño del logo</a></li>
        <li><a href="#Diseño del logo">Diseño de la herramienta</a></li>
        <li><a href="#c%C3%B3digo-en-rapid">Código en RAPID</a></li>
      </ul>
    </li>
    <li><a href="#Resultados">Resultados</a></li>
  </ol>
</details>



<!-- Planteamiento del problema -->
## Planteamiento del problema

Las redes sociales figuran en la actualidad como una de las principales formas de dar respuesta a las necesidades de los consumidores. Gigantes tecnológicos que dan cabida a todo tipo de marcas dentro de sus espacios publicitarios como Facebook, Instagram, o incluso Twitter son fundamentales en este ámbito. En el contexto de la asignatura de robótica, y considerando lo anterior, se escogió a esta última empresa para el diseño de su logotipo en el entorno del laboratorio.

En los siguientes apartados se identifican los aspectos que fueron necesarios para lograr el diseño en simulación y en el robot real de manera satisfactoria.

<!-- GETTING STARTED -->
## Desarrollo

### Diseño del logo

En primera instancia, según los parámetros definidos en la guía de laboratorio, se realizó en Inventor el característico diseño del logo de Twitter, conformado por la silueta de un monarca nuquinegro. A continuación se observa el diseño realizado, con las iniciales de los integrantes.

![Diseño CAD del logo junto a iniciales en el tablero](/Recursos/Workspacev3.png)

### Diseño de la herramienta

Se decidió realizar un diseño sencillo para la herramienta donde se ubicó el marcador, con un ángulo de 45° con respecto al eje del efector final. Las dimensiones de la herramienta se incluyen en la sección de Recursos, donde se encuentra un plano de la misma

![Herramienta](/Recursos/Herramienta.png)

La impresión de la herramienta, con el marcador posicionado se muestra a continuación.

![Herramienta](/Recursos/herramientaReal.jpg)


### Configuración de la estación virtual

En la siguiente imagen se aprecia la ubicación de los elementos dispuestos en la estación. El equipo de trabajo decidió hacerlo sobre una superficie horizontal elevada con respecto a la base del robot.

![Vista de planta de los elementos dispuestos en la estación ](/Recursos/vistaPlanta.png)

### Planteamiento de la solución

Para hacer el código de la rutina se formuló el siguiente flujo de trabajo:

![DFlujo](/Recursos/DFlujo.png)


### Código en RAPID

A partir del modelo del tablero, se procedió a definir el Workobject para trazar la trayectoria correspondiente. Fundamentalmente, se hizo uso de los comandos MoveL, MoveJ y MoveC.

`MoveL`: mueve el robot siguiendo una trayectoria lineal  
`MoveJ`: mueve el robot mediante un movimiento de ejes  
`MoveC`: mueve el robot en una trayectoria circular 

De igual forma, se hizo uso de ciclos condicionales donde, dependiendo de la entrada digital habilitada, se realizaba el diseño del tablero (D01), o se retomaba la posición de mantenimiento (D02).  
No está de más señalar, que en cuanto a los parámetros de z, se usó z0 para lograr una mayor precisión en el trazo final, que si bien definido como mínimo en z10 en la guía, el profesor indicó que podría realizarse de esta manera.

```rapid
MODULE Module1
    PERS tooldata THerramienta:=[TRUE,[[84.853,0,134.853],[0.923879533,0,0.382683432,0]],[0.1,[23.11,0,61.258],[1,0,0,0],0,0,0]];
    TASK PERS wobjdata Workobject_1:=[FALSE,TRUE,"",[[0,0,10],[1,0,0,0]],[[409.583,-9.692,240],[0,1,0,0]]];
    CONST robtarget Target_MM:=[[290.713816879,-34.485338984,-399.373982496],[0.041038912,0.230927375,0.344436207,0.909039083],[0,-1,0,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_HH:=[[169.853003696,-95,-377.146975726],[0,0.382683414,0,0.92387954],[0,0,0,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_5:=[[172.146,169.721,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_10:=[[172.146,169.721,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_15:=[[94.179,126.363,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_20:=[[95.464,37.16,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_25:=[[97.319,60.55,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_30:=[[108.141,81.369,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_35:=[[114.101,64.13,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_40:=[[128.91,53.479,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_45:=[[128.569,60.297,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_50:=[[129.686,67.033,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_55:=[[140.077,49.513,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_60:=[[159.408,43.089,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_65:=[[156.802,49.64,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_70:=[[156.139,56.659,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_75:=[[174.493,43.802,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_80:=[[196.643,47.198,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_85:=[[173.907,75.001,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_90:=[[164.745,109.728,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_95:=[[198.416,125.037,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_100:=[[192.364,161.526,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_105:=[[195.069,171.202,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_110:=[[199.539,180.201,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_115:=[[190.171,175.306,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_120:=[[183.068,167.479,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_125:=[[184.555,176.204,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_130:=[[187.549,184.533,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_135:=[[179.202,177.798,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_138:=[[200,225,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_140:=[[200,225,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_150:=[[200,240,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_155:=[[150,290,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_160:=[[100,240,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_170:=[[100,225,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_175:=[[105,392.992,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_180:=[[105,392.992,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_185:=[[150,321.197,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_190:=[[195,392.992,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_195:=[[195,392.992,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    PROC main()
        Reset DO_01;
        Reset DO_02;
        WHILE TRUE DO
            IF DI_01=1 THEN
                Set DO_01;
                Twitter;
                Reset DO_01;
            ENDIF
            IF DI_02=1 THEN
                Set DO_02;
                Path_40;
                Reset DO_02;
            ENDIF
        ENDWHILE
    ENDPROC
    PROC Path_40()
        MoveJ Target_MM,v600,z0,THerramienta\WObj:=Workobject_1;
    ENDPROC
    PROC Twitter()
        MoveJ Target_HH,v600,z0,THerramienta\WObj:=Workobject_1;
        MoveJ Target_5,v600,z5,THerramienta\WObj:=Workobject_1;
        MoveL Target_10,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_15,Target_20,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_25,Target_30,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_35,Target_40,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_45,Target_50,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_55,Target_60,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_65,Target_70,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_75,Target_80,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_85,Target_90,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_95,Target_100,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_105,Target_110,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_115,Target_120,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_125,Target_130,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_135,Target_10,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_5,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_138,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_140,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_150,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_155,Target_160,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_170,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_140,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_138,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_175,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_180,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_185,Target_190,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_195,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveJ Target_HH,v600,z0,THerramienta\WObj:=Workobject_1;
    ENDPROC
ENDMODULE
```
## Resultados

### Robot en funcionamiento - Robot Studio

<iframe width="500" height="281"  src="https://www.youtube.com/embed/IRyxWnemi_k" title="RSLab1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Robot en funcionamiento - Entorno de laboratorio

En el video de demostración del robot real, se puede observar que el movimiento del mecanismo es congruente con lo establecido en la estación virtual en Robot Studio, tanto en la trayectoria, como en el funcionamiento de las entradas digitales. 

<iframe width="500" height="281" src="https://www.youtube.com/embed/8ak_B7RKMWM" title="PruebaTwitter" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

El diseño resultante de la prueba realizada fue el siguiente. Si bien se puede identificar que parte de la cola y el ala del pájaro no tienen un trazo sólido, esto se debió principalmente a que la punta del marcador se hundió dentro de sí mismo. Al no contar con otro, fue necesario usar este como definitivo.

![Diseño CAD del logo junto a iniciales en el tablero](/Recursos/twitter.jpg)

##  Conclusiones

1. La utilización de herramientas de simulación, como Robot Studio, permitió validar el diseño del logo y la programación del robot antes de llevarlo al entorno físico. Esto ayuda a minimizar errores y optimizar el tiempo de trabajo.
2. La práctica integró conocimientos de diseño CAD, programación en RAPID y manipulación de herramientas robóticas. Esta integración demuestra la importancia de tener habilidades multidisciplinarias en el campo de la ingeniería mecatrónica.
3. La comparación entre los resultados obtenidos en la simulación y en el entorno real del laboratorio validó la efectividad del diseño y la programación del robot. Esto subraya la importancia de realizar pruebas experimentales para corroborar la funcionalidad de los sistemas robóticos.
4. La práctica permitió identificar áreas de mejora en el proceso de diseño de la herramienta y programación del robot, lo que abre oportunidades para optimizar y perfeccionar futuros proyectos similares.