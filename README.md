[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=m25210045-svg/Practica3GD)


# Práctica 3: Liberación controlada de fármacos por hidrogeles

## Información del estudiante
Vincent Alejandro Villela Salinas \[M25210045]; M25210045@tectijuana.edu.mx

Gemelos Digitales

Sistemas dinámicos y control

## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura
La asignatura de Gemelos Digitales forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Formula el gemelo digital a través de datos experimentales para el desarrollo estrategias de control mediante teorías de sistemas dinámicos no lineales y la experimentación in silico. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional.

En el contexto de sistemas dinámicos que describen sistemas biológicos o fisiológicos, el modelizado in silico es una extensión lógica de la experimentación in vitro controlada, es el resultado natural del gran aumento de la potencia computacional disponible a un costo que disminuye continuamente, combinando las ventajas de la experimentación in vivo e in vitro, sin someterse a las consideraciones éticas y la falta de control asociadas con los experimentos in vivo. A diferencia de los experimentos in vitro, que existen de forma aislada, los modelos in silico permiten incluir un conjunto prácticamente ilimitado de variables y parámetros, lo que hace que los resultados sean más aplicables en problemas del mundo real. La experimentación in silico ha dado lugar al paradigma denominado como "gemelos digitales" (en inglés digital twins); en esencia, los gemelos digitales son una réplica o representación digital de un proceso o sistema del mundo real, donde por replica se refiere a un modelo computacional desarrollado con base en datos experimentales y características especiales que le permiten conectar lo físico con lo virtual con el propósito de mejorar el rendimiento de un sistema, detectar y prevenir fallas, y realizar predicciones sobre su respuesta ante diferentes estímulos o escenarios de operación; una definición más formal establece que: un gemelo digital es un conjunto de modelos adaptativos que emulan el comportamiento de un sistema físico en un sistema virtual obteniendo datos en tiempo real para actualizarse a lo largo de su ciclo de vida; replica al sistema físico para predecir fallas y oportunidades de cambio, prescribir acciones en tiempo real para optimizar y/o mitigar eventos inesperados observando y evaluando el perfil operativo del sistema. En el campo particular de la Biología de Sistemas, un gemelo digital se presenta como un algoritmo o conjunto de algoritmos computacionales desarrollados con base en modelos mecanicistas de un organismo vivo, esto con el objetivo de emular su fisiología para ilustrar su dinámica en el corto y en el largo plazo, así como predecir su respuesta a diferentes estímulos endógenos y exógenos.

## Objetivo y descripción del sistema
Determinar la tasa de liberación del hidrogel N36 2MBA3 con base en datos experimentales.

El sistema está dado por la siguiente ecuación en el tiempo

	x(t) = rho1*t / rho2+t,  (1)

y la siguiente ecuación diferencial
	
	dx/dt = rho1 - rho2*x1. (2)

Palabras clave: Hidrogel, N45-2MBA12, N32, N35-VP15, N36-NMB3.

## Actividades a realizar  
1. Utilizar Graph Grabber para convertir los registros de la Figura 9 del artículo "Gonzáles-Ayón, Sañudo-Barajas, Picos-Corrales, and Licea-Claverie. PNVCL-PEGMA Nanohydrogels with Tailored Transition Temperature for Controlled Delivery of 5-Fluorouracil. Journal of polymer science, 2015" en series de tiempo, donde x(t): time (min), y(t): cumulative drug release (%).
2. Desarrollar un algoritmo en MATLAB que permita realizar el procesamiento de los datos, es decir, obtener bioestadísticas y graficar los datos de la actividad 1.
3. Aplicar función de peppas, función farmacocinética, función en el tiempo y una ecuación diferencial para graficar los datos obtenidos en la actividad 1.

## Lista de archivos incluidos en el repositorio
1. Cuaderno computacional de MATLAB [.mlx].
2. Archivos eureqa (ecuación en el tiempo y ecuación diferencial) [.fxp].
3. Imagénes de las simulaciones [.pdf].
4. Datos del comportamiento de los hidrogeles [.csv].
5. Imagen de tasa de liberación de hidrogeles [.png].

## Referencias
\[1] M. A. González‐Ayón, J.A. Sañudo‐Barajas, L.A. Picos‐Corrales, & A. Licea‐Claverie, "PNVCL‐PEGMA nanohydrogels with tailored transition temperature for controlled delivery of 5‐fluorouracil", Journal of Polymer Science Part A: Polymer Chemistry, vol. 53, issue 22, pp. 2662-2672, Aug 2015. DOI: https://doi.org/10.1002/pola.27766
