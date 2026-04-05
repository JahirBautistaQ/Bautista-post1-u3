# Bautista-post1-u3
Actividad Post-Contenido 1 / Unidad 3

# Bautista-post1-u3
Actividad Post-Contenido 1 / Unidad 3

Sistema de Tienda con Patrones Estructurales

Proyecto académico — Patrones de Diseño

Este proyecto implementa una simulación de una tienda utilizando Spring Boot + Maven, aplicando los patrones estructurales Adapter y Composite.

Estructura del Proyecto
tienda-patrones-estructurales/
├── pom.xml
└── src/
 ├── main/
 │ └── java/com/universidad/tienda/
 │    ├── TiendaApp.java
 │    ├── adapter/
 │    ├── composite/
 │    └── servicio/
 └── test/
     └── java/com/universidad/tienda/
         └── TiendaServicioTest.java

Requisitos
Java 17
Maven 3.8+
VS Code o IntelliJ (opcional)

Cómo ejecutar el proyecto
1. Compilar el proyecto
mvn clean package
2. Ejecutar la aplicación
mvn spring-boot:run

O también:

java -jar target/tienda-patrones-estructurales-1.0.0.jar

Ejecutar pruebas
mvn test

Resultado esperado:

BUILD SUCCESS
Tests run: 4, Failures: 0, Errors: 0

Patrones de Diseño Implementados

Adapter

Permite integrar diferentes pasarelas de pago con una interfaz común.

Clases:

PasarelaPago (Target)
PayPalAPI y StripeAPI (Adaptees)
PayPalAdapter y StripeAdapter (Adapters)

Funcionamiento:
El sistema puede cambiar de pasarela sin modificar la lógica principal:

public TiendaServicio(@Qualifier("stripe") PasarelaPago pasarela)

Composite

Permite manejar productos individuales y categorías de forma uniforme.

Clases:

ItemCatalogo (Component)
Producto (Leaf)
Categoria (Composite)

Funcionamiento:
Se construyen estructuras jerárquicas como:

Catálogo General
 ├── Electrónica
 │    ├── Computadores
 │    │    ├── Laptop
 │    │    └── MacBook
 │    └── Audífonos
 └── Libros

Funcionalidades

✔ Construcción de catálogo jerárquico
✔ Cálculo automático de precios totales
✔ Integración con múltiples pasarelas de pago
✔ Inyección de dependencias con Spring
✔ Pruebas unitarias con JUnit 5

Checkpoints de Verificación

✔ El proyecto compila sin errores (mvn clean package)
✔ La aplicación imprime el catálogo completo
✔ El pago se procesa correctamente (Stripe o PayPal)
✔ Los 4 tests unitarios pasan (mvn test — BUILD SUCCESS)
✔ El repositorio contiene commits descriptivos
✔ Este README documenta ejecución y patrones

Pruebas Incluidas
✔ Pago exitoso con PayPal
✔ Validación de token en Stripe
✔ Cálculo de precio total
✔ Estructura composite anidada

Autor

Jahir Bautista
Universidad de Santander — Cúcuta
Proyecto: Sistema de Tienda con Patrones Estructurales

