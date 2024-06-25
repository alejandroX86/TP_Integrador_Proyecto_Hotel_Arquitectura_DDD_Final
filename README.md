# Proyecto Hotel

## Descripción

El proyecto Hotel es una aplicación de gestión de clientes y reservas para un hotel, diseñada utilizando la arquitectura de Diseño Dirigido por el Dominio (DDD). Esta arquitectura permite una separación clara de responsabilidades y facilita la mantenibilidad y escalabilidad del sistema, asegurando que la lógica de negocio esté bien encapsulada y sea independiente de los detalles de implementación.

## Arquitectura DDD

El Diseño Dirigido por el Dominio (DDD) es una metodología de desarrollo de software que enfatiza la importancia de crear un modelo de dominio rico y la interacción entre diferentes componentes del sistema. En el proyecto Hotel, la arquitectura DDD se implementa a través de varias capas bien definidas:

### Capas del Sistema

1. **Capa de Presentación**: Interactúa con el usuario final y maneja la entrada y salida de datos.
2. **Capa de Aplicación**: Orquesta la lógica de aplicación y los casos de uso del sistema.
3. **Capa de Dominio**: Contiene la lógica de negocio central, entidades, repositorios y objetos de valor.
4. **Capa de Persistencia**: Maneja la persistencia de datos en diferentes tipos de bases de datos.

### Descripción de las Capas y Clases

#### Capa de Presentación

La capa de presentación es responsable de la interacción con el usuario. Aquí se definen las clases que manejan la interfaz de usuario, como `ClienteUI` y `ReservaUI`, que muestran menús y opciones para gestionar clientes y reservas.

#### Capa de Aplicación

Esta capa contiene los casos de uso del sistema, encapsulando la lógica específica de la aplicación. Las clases como `CrearClientes`, `ListarClientes`, `BorrarCliente`, `CrearReserva`, `ListarReservas`, y `BorrarReserva` se encargan de las operaciones principales del negocio.

#### Capa de Dominio

La capa de dominio es el núcleo de la aplicación, donde se define la lógica de negocio central. Aquí encontramos las entidades principales (`Cliente` y `Reserva`), los repositorios y los objetos de valor. Esta capa es independiente de los detalles de infraestructura y persiste a través de interfaces.

#### Capa de Persistencia

La capa de persistencia maneja la interacción con las bases de datos. Implementa los repositorios definidos en la capa de dominio, asegurando que las entidades puedan ser almacenadas y recuperadas de manera eficiente.

### Principios SOLID

El proyecto sigue los principios SOLID para asegurar una arquitectura limpia y mantenible:

1. **Single Responsibility Principle (SRP)**: Cada clase tiene una única responsabilidad.
2. **Open/Closed Principle (OCP)**: Las clases están abiertas para extensión pero cerradas para modificación.
3. **Liskov Substitution Principle (LSP)**: Las subclases deben poder sustituir a sus superclases sin alterar el correcto funcionamiento del programa.
4. **Interface Segregation Principle (ISP)**: Se prefieren interfaces pequeñas y específicas a interfaces grandes y multipropósito.
5. **Dependency Inversion Principle (DIP)**: Las clases de alto nivel no deben depender de clases de bajo nivel, ambas deben depender de abstracciones.

## Instalación

### Prerrequisitos

- .NET SDK (versión 5.0 o superior)
- Un editor de código, como Visual Studio o Visual Studio Code

### Clonación del Repositorio

```sh
git clone https://github.com/tu-usuario/proyecto-hotel.git
cd proyecto-hotel
