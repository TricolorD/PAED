# PAED
Motor intérprete de dimensiones basado en matrices precalculadas.

Mediante este proceso es posible crear matrices que contengan la geometría de un objeto, a partir de objetos 3D, registrando sus puntos desde la superficie de una esfera que lo envuelve.

Un objeto 3D complejo puede representarse a partir de varios trozos si estos trozos se ubican dentro de una esfera, registrando así su geometría completa, como se hace en 3D con objetos dinámicos que requieren cierta complejidad.

Sustituir las mallas de vectores por matrices puede aliviar los cálculos muy significativamente ya que la forma en la que se plantea ir de la malla a la impresión, requiere un precálculo universal a partir de un aprendizage automático que prevé la ubicación de los puntos en el área del círculo de impresión 2D, donde se representan los puntos registrados en la malla, que pertenecen a la superficie del objeto 3D de origen.

Una pantalla es un área rectanular que contiene una matriz de píxeles, donde se imprimen los gráficos formando representaciones de objetos 3D en el plano visible.
En el interior de un círculo se centra el área rectangular que corresponde con la resolución de la pantalla, dentro de este círculo base, tomaremos el espacio interior del rectángulo como área visible y así se podrán dibujar las escenas en pantalla.

El sistema requiere de varias partes.
1. la escena original en 3D.
   Esta escena va estar fomada por esferas y objetos 3D, de tal manera que los objetos 3D que se precisen, se inscribirán dentro de esferas.
2. El sistema de registro
   En este proceso se van a tomar todas las esferas de la escena como referencias. Cada esfera registrará la geometría del objeto en su interior, generando así los planos o matrices que contienen las geometrías.
3. Una esfera representa la escena. en esta escena se registran las posiciones de todas las esferas y estas tendrán una orientación de origen que posteriormente será modificada en función de la animación o punto de vista del observador.
4. Las mallas van a registrarse como matrices de texto, donde se registran las medidas a distintos puntos de la geometría 3D de cada objeto.
5. Cada geometría tendrá un plano UV, donde se agregará más información de la superficie. Reduciendo de esta manera el cálculo de mallas 3D. Los puntos de registro de la matriz van a servir de guía para modificar la colocación de la información UV y otro plano superpuesto al UV va a representar los distintos materiales.
6. La asignación de materiales se consigue mediante la definición de áreas y enumeración de materiales previamente definidos. Cada material tiene un número de indizado con propiedades de color, elasticidad, viscosidad, grosor, translucencia, refractividad...
De esta forma, al ubicar un punto de la matriz en el lugar correcto, se va a contemplar su color final y propiedades de material para reaccionar en función a los puntos de su alrededor si son del mismo material o no y deformando el UV en relación a los puntos de la matriz de registro para representar el objeto 3D y sus detalles con la mayor fidelidad y menor uso de recursos.

Las esferas de 4 ejes van aservir para asignar un eje de coordenadas al plano matriz, de este modo se puede imprimir el objeto mapeado en el interior del círculo correspondiente en la orientación requerida, cuando el punto de vista lo determine. 
