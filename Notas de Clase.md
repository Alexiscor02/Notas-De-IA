## Inteligencia Artificial 

¿Qué es la IA?
Es un campo de la informática que se encarga de crear sistemas que imiten la inteligencia artificial. La IA utiliza algoritmos y modelos matemáticos para procesar datos y tomar decisiones.

Es el desarrollo de agentes racionales.

Es el desarrollo de agentes que al interactuar con un entorno (y posiblemente otras agentes) maximice la esperanza de una utilidad futura.

## Interactuar racionalmente
- Maximizar la utilidad esperada (no se puede mejorar lo que no se puede medir),
- Con las mediciones disponibles (racional != omnisciente)
- Con las acciones posibles (racional != clarividente)
- Con lo que se conoce del entorno (racional implica exploración, aprendizaje y autonomía).

    *Racional no significa exitoso ni perfecto*

## Lo que debe saber el agente del entorno 
- Medida de desempeño/utilidad (performance)
	 Define cómo se evalúa el éxito del agente en el entorno. Por ejemplo, en un agente aspiradora, puede ser la cantidad de suciedad eliminada en un tiempo dado. Es importante que esta medida esté alineada con los objetivos del sistema.
- Características del entorno
	 
- Actuadores
	 Los mecanismos o dispositivos que permiten al agente interactuar con el entorno. Estos varían dependiendo del propósito del agente y pueden incluir:
		- Brazos robóticos.
		- Motores para movimiento.
		- Interfaces de comunicación (para agentes virtuales).
- sensores
	   Los dispositivos o medios a través de los cuales el agente percibe el entorno. Estos determinan qué información está disponible para el agente, como:
		- Cámaras para visión.
		- Micrófonos para sonido.
		- Sensores táctiles, térmicos o químicos.
		- Información de entrada de sistemas digitales, como datos de usuarios o lecturas de sistemas.
        
	Peas

## Características del entorno 
- Discreto / Continuo 
		- **Discreto:** El entorno tiene un número finito de estados, acciones o eventos. Ejemplo: un juego de ajedrez.
		- **Continuo:** Los estados o acciones están en un rango infinito o no pueden ser contados fácilmente. Ejemplo: el control de un dron en el espacio aéreo.
- Estático / Dinámico
		- **Estático:** El entorno no cambia mientras el agente toma decisiones. Ejemplo: resolver un rompecabezas.
		- **Dinámico:** El entorno puede cambiar mientras el agente toma decisiones, independientemente de sus acciones. Ejemplo: el tráfico en una ciudad.
- Observable / Parcialmente observable
		- **Completamente observable:** El agente tiene acceso a toda la información relevante del entorno. Ejemplo: un tablero de ajedrez.
		- **Parcialmente observable:** El agente solo tiene acceso a una parte de la información, lo que puede llevar a incertidumbre. Ejemplo: un robot en un laberinto con paredes bloqueando la vista.
- Determinista / Estocástico
		- **Determinista:** Cada acción del agente tiene un resultado predecible y fijo. Ejemplo: un programa que simula matemáticas exactas.
		- **Estocástico:** Las acciones del agente tienen resultados inciertos o probabilísticos. Ejemplo: lanzar un dado.
- Conocido / Desconocido
		- **Conocido:** Las reglas del entorno y sus dinámicas son conocidas de antemano por el agente.
		- **Desconocido:** El agente debe aprender las reglas o dinámicas del entorno mediante experiencia o exploración. 
- Un agente / Multiagente
		- **Un agente:** Solo un agente interactúa con el entorno. Ejemplo: resolver un rompecabezas.
		- **Multiagente:** Varios agentes interactúan entre sí, lo que puede implicar cooperación o competencia. Ejemplo: un videojuego multijugador.
- Episódico / Secuencial
		- **Episódico:** Las acciones del agente no afectan futuros episodios, y cada decisión es independiente. Ejemplo: clasificar imágenes.
		- **Secuencial:** Las acciones actuales afectan estados futuros, y las decisiones deben tener en cuenta su impacto a largo plazo. Ejemplo: conducir un automóvil.