# Patrones de Diseño

## Patrones Creacionales

### 1. Singleton
- **Qué hace**: Garantiza que una clase solo tenga una instancia y proporciona un punto de acceso global a esa instancia.
- **Ejemplo**: Gestor de conexiones a bases de datos, Logger (registro de logs).
- **Ventajas**:
  - Control estricto sobre la creación de instancias.
  - Uso eficiente de recursos compartidos.
- **Desventajas**:
  - Dificulta las pruebas unitarias debido a su naturaleza global.
  - Puede violar el principio de responsabilidad única.
- **Alternativas**: Fábrica simple o inyección de dependencias.
- **Casos de uso**: Bases de datos, sistemas de logs, gestores de configuración.

### 2. Factory Method
- **Qué hace**: Define una interfaz para crear objetos, pero permite que las subclases decidan qué clase concreta instanciar.
- **Ejemplo**: Clases que representan vehículos, como autos y camiones.
- **Ventajas**:
  - Promueve el principio de inversión de dependencias.
  - Permite la creación de objetos sin acoplamiento fuerte con clases concretas.
- **Desventajas**:
  - Puede introducir una mayor cantidad de clases debido a las subclases creadoras.
- **Alternativas**: Abstract Factory si necesitas crear familias de objetos.
- **Casos de uso**: Cuando una clase no puede anticipar la clase de los objetos que debe crear.

### 3. Abstract Factory
- **Qué hace**: Proporciona una interfaz para crear familias de objetos relacionados o dependientes sin especificar las clases concretas.
- **Ejemplo**: Componentes de GUI (ventanas, botones) para distintos sistemas operativos (Windows, MacOS, Linux).
- **Ventajas**:
  - Garantiza la compatibilidad entre los productos creados.
  - Permite sustituir fácilmente una familia de productos.
- **Desventajas**:
  - Aumenta la complejidad debido a la creación de más interfaces y clases.
- **Alternativas**: Factory Method si solo necesitas crear un tipo de objeto.
- **Casos de uso**: Sistemas modulares que necesitan configurarse dinámicamente, como sistemas de interfaces gráficas.

### 4. Builder
- **Qué hace**: Separa la construcción de un objeto complejo de su representación, permitiendo que el mismo proceso de construcción pueda crear diferentes representaciones.
- **Ejemplo**: Construcción de un automóvil con configuraciones personalizadas (color, motor, etc.).
- **Ventajas**:
  - Mejora la claridad en la construcción de objetos complejos.
  - Permite la reutilización del proceso de construcción.
- **Desventajas**:
  - Aumenta la complejidad cuando solo se necesita construir un objeto simple.
- **Alternativas**: Constructor estándar si el objeto no es tan complejo.
- **Casos de uso**: Creación de objetos con múltiples configuraciones, como un formulario complejo o un asistente de instalación.

### 5. Prototype
- **Qué hace**: Permite copiar objetos existentes sin que el código dependa de sus clases.
- **Ejemplo**: Duplicación de objetos en videojuegos (enemigos, edificios).
- **Ventajas**:
  - Mejora el rendimiento al evitar la creación de objetos desde cero.
  - Elimina la necesidad de conocer la clase exacta del objeto.
- **Desventajas**:
  - Puede ser difícil implementar la clonación en objetos complejos.
- **Alternativas**: Factory Method si no es necesario clonar instancias existentes.
- **Casos de uso**: Duplicación de objetos configurados, como formularios predefinidos o estados guardados en juegos.

## Patrones Estructurales

### 6. Adapter
- **Qué hace**: Permite que clases con interfaces incompatibles trabajen juntas mediante una clase intermediaria que actúa como traductora.
- **Ejemplo**: Integración de una nueva biblioteca de gráficos con un sistema antiguo.
- **Ventajas**:
  - Facilita la reutilización de código existente.
  - Mejora la flexibilidad al separar interfaces y lógica.
- **Desventajas**:
  - Puede aumentar la complejidad del código.
- **Alternativas**: Facade si solo deseas simplificar una interfaz compleja.
- **Casos de uso**: Integración de sistemas antiguos con nuevas bibliotecas o tecnologías.

### 7. Bridge
- **Qué hace**: Desacopla una abstracción de su implementación, permitiendo que ambas evolucionen de manera independiente.
- **Ejemplo**: Sistema de controles remotos que puede ser utilizado en televisores de diferentes marcas.
- **Ventajas**:
  - Permite cambiar o extender las implementaciones sin afectar a las abstracciones.
  - Favorece la flexibilidad y la escalabilidad.
- **Desventajas**:
  - Introduce más clases y capas, lo que puede complicar el diseño.
- **Alternativas**: Strategy si deseas variar comportamientos dinámicamente.
- **Casos de uso**: Interfaces gráficas que deben funcionar con múltiples dispositivos o bases de datos.

### 8. Composite
- **Qué hace**: Compone objetos en estructuras de árbol para representar jerarquías parte-todo, permitiendo que los clientes traten a los objetos individuales y compuestos de manera uniforme.
- **Ejemplo**: Sistemas de menús en aplicaciones, donde cada menú puede contener submenús.
- **Ventajas**:
  - Permite tratar a los objetos y las composiciones de manera uniforme.
  - Facilita la gestión de estructuras jerárquicas complejas.
- **Desventajas**:
  - La complejidad del código puede aumentar si no se maneja bien.
- **Alternativas**: Decorator si solo quieres agregar comportamientos adicionales.
- **Casos de uso**: Representación de estructuras jerárquicas como archivos y carpetas, menús y submenús.

### 9. Decorator
- **Qué hace**: Agrega responsabilidades adicionales a un objeto de manera dinámica sin alterar su estructura.
- **Ejemplo**: Sistema de cafés, donde se pueden agregar ingredientes adicionales (como leche o chocolate) sin cambiar la clase del café.
- **Ventajas**:
  - Ofrece una forma flexible de extender la funcionalidad de objetos individuales.
  - Cumple con el principio de responsabilidad única.
- **Desventajas**:
  - Aumenta la complejidad del código debido a la gran cantidad de clases envoltorio.
- **Alternativas**: Usar herencia si las responsabilidades adicionales son conocidas de antemano.
- **Casos de uso**: Sistemas de personalización de productos, como configuraciones de autos o pedidos de café.

### 10. Facade
- **Qué hace**: Proporciona una interfaz simplificada a un conjunto de interfaces en un subsistema.
- **Ejemplo**: Proporcionar una interfaz simple para trabajar con un sistema complejo de bibliotecas gráficas.
- **Ventajas**:
  - Reduce la complejidad para los usuarios del subsistema.
  - Separa los detalles de implementación de la interfaz pública.
- **Desventajas**:
  - Puede ocultar demasiada funcionalidad del sistema subyacente.
- **Alternativas**: Adapter si necesitas ajustar la interfaz existente.
- **Casos de uso**: Simplificación de bibliotecas complejas o sistemas de trabajo en múltiples capas.

### 11. Flyweight
- **Qué hace**: Usa el almacenamiento compartido para minimizar el uso de memoria por objetos similares.
- **Ejemplo**: Sistemas de gráficos donde muchos objetos comparten la misma representación visual.
- **Ventajas**:
  - Ahorra memoria y mejora el rendimiento.
  - Reduce la duplicación de datos.
- **Desventajas**:
  - Puede complicar la gestión del estado de los objetos compartidos.
- **Alternativas**: Singleton si necesitas una única instancia global.
- **Casos de uso**: Sistemas gráficos, procesamiento de texto donde múltiples caracteres comparten la misma representación.

### 12. Proxy
- **Qué hace**: Proporciona un sustituto o representante de otro objeto para controlar el acceso a este.
- **Ejemplo**: Proxy de seguridad que controla el acceso a un objeto real.
- **Ventajas**:
  - Proporciona control sobre el acceso a objetos sensibles o costosos de crear.
  - Puede mejorar el rendimiento con proxies perezosos o remotos.
- **Desventajas**:
  - Introduce complejidad adicional en el sistema.
- **Alternativas**: Facade si solo necesitas simplificar una interfaz.
- **Casos de uso**: Control de acceso, proxies de seguridad, proxies remotos.

## Patrones Comportamentales

### 13. Chain of Responsibility
- **Qué hace**: Permite que más de un objeto maneje una petición, pasando la petición a lo largo de una cadena de manejadores.
- **Ejemplo**: Sistema de manejo de solicitudes de soporte, donde diferentes niveles de soporte pueden manejar la solicitud.
- **Ventajas**:
  - Desacopla los emisores de las solicitudes de los manejadores.
  - Ofrece flexibilidad para agregar o eliminar manejadores.
- **Desventajas**:
  - No garantiza que la solicitud será manejada.
- **Alternativas**: Command si deseas encapsular las solicitudes en objetos.
- **Casos de uso**: Manejo de eventos o solicitudes jerárquicas como sistemas de atención al cliente.

### 14. Command
- **Qué hace**: Encapsula una petición como un objeto, permitiendo parametrizar a los clientes con distintas peticiones.
- **Ejemplo**: Un sistema de menú que permite deshacer y rehacer acciones.
- **Ventajas**:
  - Proporciona un mecanismo para deshacer y rehacer operaciones.
  - Desacopla al cliente que emite las peticiones del objeto que las ejecuta.
- **Desventajas**:
  - Aumenta el número de clases al tener que definir una clase de comando para cada acción.
- **Alternativas**: Mediator si deseas controlar la interacción entre varios objetos.
- **Casos de uso**: Sistemas con operaciones que necesitan ser deshechas o aplazadas, como editores de texto o sistemas transaccionales.

### 15. Interpreter
- **Qué hace**: Dada una gramática, define una representación para interpretar sentencias en dicho lenguaje.
- **Ejemplo**: Interpretación de expresiones matemáticas o lenguajes específicos de dominio.
- **Ventajas**:
  - Proporciona una forma estructurada para evaluar o interpretar expresiones.
- **Desventajas**:
  - El uso de este patrón puede ser ineficiente para gramáticas complejas.
- **Alternativas**: Usar un parser o compilador si el lenguaje es demasiado complejo.
- **Casos de uso**: Lenguajes específicos de dominio o motores de reglas.

### 16. Iterator
- **Qué hace**: Proporciona una forma de acceder secuencialmente a los elementos de un agregado sin exponer su representación subyacente.
- **Ejemplo**: Recorriendo una lista de elementos o una colección.
- **Ventajas**:
  - Simplifica el recorrido de colecciones complejas.
  - Aísla la lógica de recorrido de la lógica de la colección.
- **Desventajas**:
  - Puede no ser eficiente si se utiliza en colecciones muy grandes sin optimización.
- **Alternativas**: Foreach loops si la colección es sencilla.
- **Casos de uso**: Recorrido de listas, árboles o colecciones en general.

### 17. Mediator
- **Qué hace**: Define un objeto que encapsula cómo interactúan un conjunto de objetos, promoviendo el desacoplamiento.
- **Ejemplo**: Un sistema de chat donde el servidor actúa como mediador entre los usuarios.
- **Ventajas**:
  - Desacopla los objetos entre sí al centralizar su interacción.
  - Facilita el mantenimiento y la escalabilidad.
- **Desventajas**:
  - El mediador puede convertirse en un punto único de fallo o cuello de botella.
- **Alternativas**: Observer si solo necesitas notificar a otros objetos de cambios en el estado.
- **Casos de uso**: Sistemas donde múltiples objetos interactúan, como interfaces gráficas o sistemas de mensajería.

### 18. Memento
- **Qué hace**: Permite capturar y externalizar el estado interno de un objeto sin violar la encapsulación, para que el objeto pueda restaurarse a ese estado más tarde.
- **Ejemplo**: Sistema de deshacer/rehacer en un editor de texto.
- **Ventajas**:
  - Facilita la implementación de operaciones de deshacer y rehacer.
  - Mantiene la encapsulación del estado del objeto.
- **Desventajas**:
  - Puede consumir mucha memoria si se almacenan demasiados estados.
- **Alternativas**: Usar Command si las operaciones son más importantes que el estado.
- **Casos de uso**: Deshacer/rehacer en aplicaciones como editores de texto o software de diseño.

### 19. Observer
- **Qué hace**: Define una dependencia de uno a muchos entre objetos, de manera que cuando uno cambia de estado, todos sus dependientes son notificados.
- **Ejemplo**: Un sistema de notificaciones en una red social, donde los seguidores son notificados de las actualizaciones.
- **Ventajas**:
  - Promueve el desacoplamiento entre el emisor de eventos y los suscriptores.
  - Facilita la implementación de sistemas reactivos.
- **Desventajas**:
  - Los observadores pueden convertirse en puntos de cuello de botella si reciben demasiadas notificaciones.
- **Alternativas**: Mediator si las interacciones entre objetos son más complejas.
- **Casos de uso**: Sistemas de notificación, eventos en interfaces gráficas, sistemas de suscripciones.

### 20. State
- **Qué hace**: Permite que un objeto altere su comportamiento cuando su estado interno cambia.
- **Ejemplo**: Una máquina expendedora que cambia su comportamiento según el saldo ingresado.
- **Ventajas**:
  - Facilita la implementación de máquinas de estados finitos.
  - Permite encapsular los estados y reducir el código condicional.
- **Desventajas**:
  - Aumenta el número de clases para representar cada estado.
- **Alternativas**: Strategy si los cambios de comportamiento no están ligados a un estado interno.
- **Casos de uso**: Sistemas de máquinas de estados, como una máquina de café o un videojuego.

### 21. Strategy
- **Qué hace**: Define una familia de algoritmos, encapsula cada uno de ellos y los hace intercambiables.
- **Ejemplo**: Algoritmos de ordenación que pueden ser intercambiados según la situación (burbuja, quicksort, mergesort).
- **Ventajas**:
  - Facilita el intercambio de comportamientos sin modificar las clases que los usan.
  - Promueve la reutilización de código y el desacoplamiento.
- **Desventajas**:
  - El cliente debe ser consciente de las diferentes estrategias disponibles.
- **Alternativas**: State si los comportamientos están directamente ligados a cambios de estado.
- **Casos de uso**: Algoritmos de ordenación, sistemas de pago con diferentes métodos, rutas en sistemas GPS.

### 22. Template Method
- **Qué hace**: Define el esqueleto de un algoritmo en una operación, diferiendo algunos pasos a las subclases.
- **Ejemplo**: Clases base que definen el flujo general del proceso de construcción de objetos, permitiendo que las subclases definan detalles específicos.
- **Ventajas**:
  - Promueve la reutilización del código base.
  - Facilita la implementación de algoritmos que comparten estructura común pero varían en detalles.
- **Desventajas**:
  - Puede ser difícil de mantener si el algoritmo base cambia frecuentemente.
- **Alternativas**: Strategy si prefieres intercambiar comportamientos completos en lugar de diferir pasos del algoritmo.
- **Casos de uso**: Sistemas de construcción de objetos, interfaces gráficas con pasos comunes.

### 23. Visitor
- **Qué hace**: Permite definir nuevas operaciones sobre una jerarquía de clases sin cambiar las clases sobre las que opera.
- **Ejemplo**: Un sistema de impuestos donde el cálculo varía según el tipo de producto (alimentos, tecnología, etc.).
- **Ventajas**:
  - Facilita la adición de operaciones sin modificar las clases base.
  - Cumple con el principio de abierto/cerrado.
- **Desventajas**:
  - Dificulta el mantenimiento cuando la jerarquía de clases cambia frecuentemente.
- **Alternativas**: Usar métodos en las propias clases si las operaciones no cambian con frecuencia.
- **Casos de uso**: Sistemas de análisis de expresiones, procesamiento de árboles de sintaxis, procesamiento de estructuras de archivos.
