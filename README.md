# Patrones de Diseño

## Patrones Creacionales

### 1. Singleton
- **Qué hace**: Asegura que una clase solo tenga una instancia y ofrece un acceso global a ella.
- **Ejemplo**: Logger, gestor de conexiones de base de datos.
- **Ventajas**: Control sobre instancias y uso eficiente de recursos.
- **Desventajas**: Dificulta pruebas unitarias y puede romper la responsabilidad única.
- **Casos de uso**: Logs, configuraciones compartidas, conexión a BD.

### 2. Factory Method
- **Qué hace**: Define una interfaz para crear objetos, dejando que las subclases elijan el tipo de objeto a crear.
- **Ejemplo**: Vehículos (autos, camiones).
- **Ventajas**: Desacopla la creación de objetos y promueve la flexibilidad.
- **Desventajas**: Aumenta la cantidad de subclases.
- **Casos de uso**: Crear objetos cuando no se conoce de antemano su clase concreta.

### 3. Abstract Factory
- **Qué hace**: Crea familias de objetos relacionados sin especificar sus clases concretas.
- **Ejemplo**: Componentes de GUI para Windows, MacOS y Linux.
- **Ventajas**: Garantiza la compatibilidad entre productos relacionados.
- **Desventajas**: Aumenta la complejidad con muchas interfaces y clases.
- **Casos de uso**: Sistemas modulares que requieren configurar familias de objetos.

### 4. Builder
- **Qué hace**: Permite construir objetos complejos paso a paso.
- **Ejemplo**: Automóviles personalizados (color, motor, accesorios).
- **Ventajas**: Facilita la creación de objetos complejos de manera legible.
- **Desventajas**: Añade complejidad innecesaria si el objeto es simple.
- **Casos de uso**: Objetos con muchas opciones de configuración.

### 5. Prototype
- **Qué hace**: Clona objetos existentes para crear nuevos, sin depender de sus clases.
- **Ejemplo**: Clonar enemigos en un videojuego.
- **Ventajas**: Mejora el rendimiento al evitar la creación desde cero.
- **Desventajas**: Difícil de implementar con objetos complejos.
- **Casos de uso**: Duplicar objetos preconfigurados.

## Patrones Estructurales

### 6. Adapter
- **Qué hace**: Permite que clases con interfaces distintas trabajen juntas.
- **Ejemplo**: Integrar una biblioteca nueva en un sistema existente.
- **Ventajas**: Reutiliza código existente y mejora la flexibilidad.
- **Desventajas**: Aumenta la complejidad del sistema.
- **Casos de uso**: Integrar sistemas antiguos con tecnologías nuevas.

### 7. Bridge
- **Qué hace**: Separa una abstracción de su implementación, permitiendo que evolucionen por separado.
- **Ejemplo**: Controles remotos que funcionan en distintos dispositivos.
- **Ventajas**: Flexibilidad al cambiar abstracción o implementación sin afectar la otra.
- **Desventajas**: Introduce más clases y capas de abstracción.
- **Casos de uso**: Sistemas que requieren ser escalables con diferentes implementaciones.

### 8. Composite
- **Qué hace**: Componer objetos en estructuras de árbol para tratar objetos individuales y compuestos de manera uniforme.
- **Ejemplo**: Menús en una aplicación, con submenús.
- **Ventajas**: Manejo sencillo de jerarquías complejas.
- **Desventajas**: Aumenta la complejidad si no se gestiona adecuadamente.
- **Casos de uso**: Representar jerarquías como carpetas y archivos.

### 9. Decorator
- **Qué hace**: Añade funcionalidades adicionales a un objeto de manera dinámica.
- **Ejemplo**: Agregar ingredientes a un café (leche, chocolate) sin cambiar la clase base.
- **Ventajas**: Extiende funcionalidad sin usar herencia.
- **Desventajas**: Aumenta la complejidad del código.
- **Casos de uso**: Personalización de objetos.

### 10. Facade
- **Qué hace**: Proporciona una interfaz simplificada para un sistema complejo.
- **Ejemplo**: Simplificar el acceso a una biblioteca gráfica.
- **Ventajas**: Reduce la complejidad para los usuarios del subsistema.
- **Desventajas**: Puede ocultar demasiada funcionalidad.
- **Casos de uso**: Simplificar subsistemas complejos.

### 11. Flyweight
- **Qué hace**: Optimiza el uso de memoria compartiendo datos entre objetos similares.
- **Ejemplo**: Representación de caracteres en un procesador de texto.
- **Ventajas**: Ahorra memoria en sistemas con muchos objetos similares.
- **Desventajas**: Complica la gestión del estado de los objetos.
- **Casos de uso**: Sistemas gráficos o texto.

### 12. Proxy
- **Qué hace**: Proporciona un intermediario para controlar el acceso a un objeto.
- **Ejemplo**: Proxy de seguridad que controla el acceso a recursos sensibles.
- **Ventajas**: Controla el acceso y mejora el rendimiento.
- **Desventajas**: Añade complejidad al sistema.
- **Casos de uso**: Control de acceso o proxies remotos.

## Patrones Comportamentales

### 13. Chain of Responsibility
- **Qué hace**: Pasa una solicitud a lo largo de una cadena de objetos hasta que se maneja.
- **Ejemplo**: Sistema de soporte técnico con distintos niveles de asistencia.
- **Ventajas**: Desacopla el remitente de la solicitud del receptor.
- **Desventajas**: No garantiza que la solicitud será manejada.
- **Casos de uso**: Manejo de eventos o solicitudes en cascada.

### 14. Command
- **Qué hace**: Encapsula una acción como un objeto para parametrizar otras acciones.
- **Ejemplo**: Menú que permite deshacer y rehacer acciones.
- **Ventajas**: Desacopla el emisor de la acción del objeto que la ejecuta.
- **Desventajas**: Aumenta la cantidad de clases.
- **Casos de uso**: Implementar deshacer/rehacer o aplazar operaciones.

### 15. Interpreter
- **Qué hace**: Define cómo interpretar sentencias en un lenguaje específico.
- **Ejemplo**: Interpretación de expresiones matemáticas.
- **Ventajas**: Proporciona una manera estructurada para evaluar expresiones.
- **Desventajas**: Ineficiente para gramáticas complejas.
- **Casos de uso**: Lenguajes específicos de dominio o motores de reglas.

### 16. Iterator
- **Qué hace**: Permite recorrer los elementos de una colección sin exponer su representación interna.
- **Ejemplo**: Recorrer una lista o un conjunto.
- **Ventajas**: Facilita el recorrido de estructuras complejas.
- **Desventajas**: Puede ser ineficiente en colecciones muy grandes.
- **Casos de uso**: Recorrer listas, árboles o cualquier colección.

### 17. Mediator
- **Qué hace**: Centraliza la comunicación entre objetos, evitando dependencias directas entre ellos.
- **Ejemplo**: Sistema de chat donde el servidor actúa como mediador.
- **Ventajas**: Desacopla los objetos entre sí, facilitando el mantenimiento.
- **Desventajas**: Puede convertirse en un cuello de botella.
- **Casos de uso**: Sistemas donde muchos objetos interactúan.

### 18. Memento
- **Qué hace**: Permite guardar el estado de un objeto para restaurarlo más tarde.
- **Ejemplo**: Función de deshacer en un editor de texto.
- **Ventajas**: Facilita la implementación de deshacer/rehacer.
- **Desventajas**: Puede consumir mucha memoria si se almacenan muchos estados.
- **Casos de uso**: Funcionalidad de deshacer/rehacer.

### 19. Observer
- **Qué hace**: Notifica a varios objetos cuando otro cambia de estado.
- **Ejemplo**: Sistema de notificaciones en redes sociales.
- **Ventajas**: Facilita la implementación de sistemas reactivos.
- **Desventajas**: Puede crear cuellos de botella si hay demasiados observadores.
- **Casos de uso**: Sistemas de notificaciones o eventos en interfaces gráficas.

### 20. State
- **Qué hace**: Permite que un objeto cambie su comportamiento cuando cambia su estado interno.
- **Ejemplo**: Máquina expendedora que ajusta su comportamiento según el saldo ingresado.
- **Ventajas**: Facilita la implementación de máquinas de estados.
- **Desventajas**: Aumenta el número de clases.
- **Casos de uso**: Máquinas de estados, como videojuegos o máquinas expendedoras.

### 21. Strategy
- **Qué hace**: Permite elegir entre diferentes algoritmos de manera dinámica.
- **Ejemplo**: Algoritmos de ordenación (burbuja, quicksort).
- **Ventajas**: Facilita el intercambio de comportamientos sin modificar el cliente.
- **Desventajas**: El cliente debe conocer las estrategias disponibles.
- **Casos de uso**: Selección de algoritmos o comportamientos dinámicos.

### 22. Template Method
- **Qué hace**: Define el esqueleto de un algoritmo, permitiendo que las subclases implementen partes específicas.
- **Ejemplo**: Clases base que definen el flujo general de construcción de objetos.
- **Ventajas**: Facilita la reutilización de la lógica común.
- **Desventajas**: Difícil de mantener si el algoritmo cambia frecuentemente.
- **Casos de uso**: Procesos con pasos comunes que varían en detalles.

### 23. Visitor
- **Qué hace**: Permite añadir nuevas operaciones a una jerarquía de clases sin modificarlas.
- **Ejemplo**: Sistema de cálculo de impuestos que varía según el tipo de producto.
- **Ventajas**: Facilita la adición de funcionalidades sin cambiar las clases base.
- **Desventajas**: Dificulta el mantenimiento si las clases cambian frecuentemente.
- **Casos de uso**: Procesamiento de estructuras complejas como árboles de sintaxis.
