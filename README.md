# 📚 API REST de Libros

API REST desarrollada en Spring Boot para la **gestión de libros**.  
Permite realizar operaciones CRUD (crear, leer, actualizar y eliminar libros), aplicando el **patrón DTO (Data Transfer Object)** para exponer solo los datos necesarios al cliente y el principio de **Inversión de Control (IoC)** mediante la **Inyección de Dependencias** usando el contenedor de Spring.


---

## ⚙️ Tecnologías Utilizadas

- Java 17  
- Spring Boot  
- Spring Web  
- Spring Data JPA  
- MySQL  
- Gradle  
- Lombok  

---

## 🎯 Objetivos del Ejercicio

- Implementar una API REST usando Spring Boot
- Aplicar el patrón DTO para transferir datos de forma controlada
- Utilizar el principio de Inversión de Control con inyección de dependencias
- Persistir datos en una base de datos MySQL usando Spring Data JPA
- Diseñar una arquitectura en capas, clara y mantenible

---

## ✨ Funcionalidades

- 📚 Crear un nuevo libro: `POST /api/books`
- 📖 Obtener todos los libros: `GET /api/books`
- 🔍 Buscar un libro por ID: `GET /api/books/{id}`
- ✏️ Editar (actualizar) un libro: `PUT /api/books/{id}`
- 🗑 Eliminar un libro: `DELETE /api/books/{id}`

---

## 🎓 Conceptos Aplicados

### 🏛️ Arquitectura en Capas

- **Controller**: expone los endpoints HTTP
- **Service**: contiene la lógica de negocio
- **Repository**: accede a la base de datos con JPA
- **Entity**: representa el modelo de datos (libros)
- **DTO**: transfiere datos al cliente
- **Mapper**: convierte entre Entity y DTO

---

### 📦 Patrón DTO (Data Transfer Object)

- Se crearon clases DTO para representar los datos que viajan desde y hacia la API.
- Los DTO se usan para controlar qué campos se exponen al cliente y separar el modelo interno del modelo expuesto.
- Por ejemplo, `BookDTO` encapsula solo `id`, `title`, `author` y `year`.

---

### 🔁 Patrón Inversión de Control (IoC)

- Aplicado usando el contenedor de Spring con anotaciones como:
  - `@Service` para la capa de servicio
  - `@Autowired` para inyectar dependencias (como servicios dentro de controladores)
- Esto permite que las clases no creen manualmente sus dependencias, sino que el framework las provea automáticamente.

---

## 🗃️ Spring Data JPA

- Se usa `BookRepository` que extiende `JpaRepository` para manejar operaciones con la base de datos.
- No se necesita escribir código SQL manual.
- Soporte automático para operaciones CRUD y consultas personalizadas.

---

## 🌐 API REST

- Uso de anotaciones `@RestController`, `@RequestMapping`, `@PostMapping`, etc.
- Los datos se envían y reciben en formato JSON.
- La comunicación entre cliente y servidor se hace usando métodos HTTP estándar: `GET`, `POST`, `PUT`, `DELETE`.

---

## 👨‍💻 Autor

Giovanni Giannoni  
Estudiante de Tecnicatura Universitaria en Programación  
Universidad Tecnológica Nacional (UTN)

---

