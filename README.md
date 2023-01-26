# PAED
Motor intérprete de dimensiones basado en matrices precalculadas.
Mediante este proceso es posible crear matrices a partir de objetos que contengan la geometría de un objeto, registrando sus puntos desde la superficie de una esfera que lo envuelve.
Un objeto 3D complejo puede representarse a partir de muchos trozos y estos trozos se ubican dentro de una esfera, registrando así su geometría completa, como se hace en 3D con objetos dinámicos que requieren cierta complejidad.
Sustituir las mallas de vectores por matrices puede aliviar los cálculos muy significativamente ya que la forma en la que se plantea ir de la malla a la impresión, requiere un precálculo universal a partir de un aprendizage automático que prevee la ubicación de los puntos en el área del círculo de impresión 2D, donde se representan los puntos registrados que pertenecen a la superficie del objeto 3D de origen.
