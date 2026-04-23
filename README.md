


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
Aplicar el sistema de Lotka-Volterra para analizar los datos registrados en la interacción de dos especies articas, liebres (presa) y linces (depredador) durante 20 años. El sistema presa-depredador se formula mediante las siguientes dos EDOs de primer orden:

	dx/dt = alpha*x - beta*x*y,  (1)
	dy/dt = delta*x*y - gamma*y, (2)

donde los valores de los parámetros alpha, beta, delta, gamma > 0, y las condiciones iniciales x(0), y(0) > 0. La descripción de las ecuaciones del sistema de Lotka-Volterra (1)-(2) se realiza a continuación. La Ecuación (1) modeliza la dinámica de la población presa en la cual el término +alpha*x define el crecimiento de esta población de manera exponencial y el término -beta*x*y describe la tasa de depredación como una proporción entre los encuentros de la población presa y los depredadores. La Ecuación (2) modeliza la evolución de los depredadores, el término +delta*x*y implica que el crecimiento de la población depredadora depende del encuentro con las presas, sin embargo, la tasa de crecimiento no necesariamente es igual a la tasa en que consumen a las presas, por eso se emplean parámetros distintos, el término - gamma*y  representa la muerte natural o emigración de los depredadores como un decrecimiento exponencial en la ausencia de presas.

Palabras clave: Hidrogel, N45-2MBA12, N32, N35-VP15, N36-NMB3.

## Actividades a realizar  
1. Utilizar Graph Grabber para convertir los registros de la Figura 1.1 del libro "Garfinkel, Alan, Jane Shevtsov, and Yina Guo. Modeling life: the mathematics of biological systems. Springer International Publishing AG, 2017" en series de tiempo, donde x(t): liebres (snowshoe hares), y(t): linces (lynx) y el tiempo t está medido en años.
2. Desarrollar un algoritmo en MATLAB que permita realizar el procesamiento de los datos, es decir, graficarlos, suavizarlos y normalizarlos.
3. Aplicar la función fitnlm de MATLAB para ajustar los datos mediante regresión no lineal por mínimos cuadrados y estimar los valores de los parámetros del modelo de Lotka-Volterra con sus respectivos bioestadísticos: Error estándar, margen de error, intervalos de confianza del 95% y valor P, además de pruebas de bondad de ajuste como el coeficiente de determinación (R²), suma residual de cuadrados (RSS) y el Criterio de Información de Akaike (AIC).
4. Comparar el efecto del paso de integración en los métodos de diferencias finitas de Euler y Heun ilustrando las soluciones en el tiempo y la trayectoria en el plano de fase.
5. Calcular los puntos de equilibrio del sistema, graficarlos en el plano de fase y analizar su estabilidad local.
6. Convertir el sistema de Lotka-Volterra a un diagrama de bloques en Simulink y comparar las funciones ode stiff y nonstiff de paso variable y las funciones de paso fijo:
	a.Stiff solvers:		
		i.ode15s. Accuracy: Low to Medium.
		ii.ode23s. Accuracy: Low.
		iii.ode23t. Accuracy: Low.
		iv.ode23tb. Accuracy: Low.
	b.Nonstiff solvers:
		i.ode45. Accuracy: Medium.
		ii.ode23. Accuracy: Low.
		iii.ode113. Accuracy: Low to High.
	c.Fixed-step
		i.ode1:Euler
		ii.ode2:Heun
		iii.ode3:Bogacki-Shampine
		iv.ode4:Runge-Kutta
		v.ode5:Dormand-Prince
7. Aplicar las funciones ode78 y ode89 para resolver el sistema de Lotka-Volterra.
8. Diseñar un diagrama biológico sobre la dinámica del sistema y la interacción entre sus variables con las figuras de https://bioart.niaid.nih.gov/ o https://www.biorender.com/.

## Lista de archivos incluidos en el repositorio
1. Cuaderno computacional de MATLAB [.mlx].
2. Modelo de Simulink [.slx].
3. Imagénes de las simulaciones [.pdf].
4. Análisis matemático [.pdf].
5. Diagrama biológico del sistema [.png].

## Referencias
\[1] P. A. Valle, Syllabus para Gemelos Digitales, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] Garfinkel, Alan, Jane Shevtsov, and Yina Guo. Modeling life: the mathematics of biological systems. Springer International Publishing AG, 2017. doi: https://doi.org/10.1007/978-3-319-59731-7. Permalink: https://sysbio.mx/wp-content/uploads/2021/02/2017_Book_ModelingLife.pdf
