## Notas de Clase

## Aprendizaje Maquina

**Motivacion**:

Es muy dificili escribir programas que resuelvan problemas complejos, ya sea por que no tenemos idea de como nuestro propio cerebro procesa la informacion, o por que, aun que supieramos, la cantidad de reglas y condiciones que tendriamos que escribir nos dejaria un codigo demasiado grande, y que ademas, en ocaciones que estemos ante un problema dinamico, tendriamos que estar actualizando las reglas continuamente.

**La solucion:**

Descartamos la idea de escribir un programa especifico para cada tarea, en en su lugar podemos recolectar muchos ejemplos que especifiquen la respuesta correcta en cada caso. Enviamos los datos al algoritmo de *aprendizaje maquina* el cual nos devuelve un programa. Si esta bien hecho debe funcionar para nuevos casos on cierto margen de confianza. Grandes cantidades de datos, y capacidad masiva de computo es mas economico actualmente que expertos en tareas especificas.

**Generalizacion:**

1. **Error en Muestra:**

   * Es el error que el modelo comete en los datos de entrenamiento.
   * Si $E_{in} \approx 0$, el modelo ha memorizado bien los datos de entrenamiento.
2. **Error fuera de muestra:**

   * Es el error del modelo en datos nuevos, nunca antes vistos.
   * Un modelo con un bajo $E_{out}$ generaliza bien.
3. **Condicion para que el aprendizaje exista:**

   * Queremos que el modelo funcione bien para datos nuevos, es decir que $E_{out} \approx 0$.
   * Esto solo ocurre si:
     * $E_{in} \approx 0 \rightarrow$ El modelo se ajusta bien a los datos de entrenamiento.
     * $E_{in} \approx E_{out} \rightarrow$ El modelo no sobreajusta, lo que significa que el error en los datos de entrenamiento es representativo del error en datos nuevos.
       * Si $E_{in} \approx 0$ pero $E_{in} \neq E_{out}$, significa que hay sobre ajuste, lo que impide la generalizacion.
       * Si $E_{in} \approx E_{out}$ pero ambos son grandes, el modelo esta infraajustando y no esta aprendiendo bien.
4. **Conclusion:**

   * Para que el aprendizaje sea exitoso, necesitamos un buen equilibrio entre ajuste y generalizacion:

     * $E_{in} \approx 0$ y $E_{in} \approx E_{out}$

Esto significa que el modelo debe ser suficientemente expresivo para capturar la estructura de los datos sin caer en la memorizacion excesiva.

## El metodo del vecino mas proximo

* Metodo no parametrico
* Requiere guardar todos los datos del conjunto de entrenamiento
* Se calcula una medida de similaridad del dato desconocido con TODOS los datos del conjunto de entrenamiento
* Se selecciona la clase del dato mas cercano No hay metodo mas simple conceptualmente

![1738302375666](image/Notas2_IA/1738302375666.png)

![1738302445421](image/Notas2_IA/1738302445421.png)

![1738302478756](image/Notas2_IA/1738302478756.png)

## Metodos de aprendizaje maquina

* Modelos descriptivos
* Modelos lineales generalizados
* Arboles de decision
* Redes neuronales
* Metodos de ensemble

## ¿En que sentido el aprendizaje supervisado es posible?

**Recapitulando:**

Decimos que $f \approx h^*$ ssi

    $E_i (h*) \approx 0$

y

    $E_0(h^*) \approx E_i(h^**)$

$E_i(h^*) \approx 0$

* Problema de optimizacion
* Encontrar $h^*$ equivale a encontrar el vector de parametros $\theta ^* $ tal que
  $ \theta ^* = arg \min_{\theta \in \Theta} \frac{1}{M} \sum_{i=1}^{M} loss(y^{(i)}, h_{\theta}(x^{(i)}))$

$E_0(h^*) \approx E_i(h^*)$

* Generalizacion
* Diferencia entre aprendizaje y optimizacion
* Vamos a usar una nocion que aparece una broma:

*Aprendizaje Probablemente Aproximadamente Correcto (PAC Learning)*

## Desiguladad de Hoeffding

$Pr[|E_0(h^*) - E_i(h^*)|\geq \epsilon] \leq 2 \exp(-2\epsilon ^2)$

donde M es el numero de datos y $\epsilon$ la diferencia entre el error en muestra y el error fuera de muestra impuesto.

**Entonces, el planteamiento $E_0(h^*) \approx E_i(h^*)$ es pac**

## Arboles de desicion

Un **arbol de desicion** es una funcion $f: X \rightarrow Y$ que asigna valores de entrada $X$ a etiquetas de salida $Y$. Se estructura de la siguiente manera:
* Cada **nodo interno** representa una desicion basada en un atributo $x_i$.
* Cada **rama** corresponde a un posible valor del atributo $x_i = v$.
* Cada **hoja** asigna una clase y, que representa la prediccion final.
* Para **clasificar** una entrada $x$, se recorre el arbol desde la raiz hasta una hoja, siguiendo las desiciones segun los valores de los atributos.

Los arboles de desicion son altamente expresivos y pueden representar cualquier funcion de los atributos de entrada:
* **Universatilidad:** Los arboles de desicion pueden modelar cualquier funcion que asigne entradas discretas  a salidas discretas.

* **Funciones Booleanas:** Cada camino desde la raiz hasta una hoja representa una fila en la tabla de verdad de una funcion Booleanda.

* **Complejidad:** Aunque pueden expresar cualquier funcion, algunas pueden requerir un **numero exponencial de nodos**, lo que los hace ineficientes en ciertos casos.



