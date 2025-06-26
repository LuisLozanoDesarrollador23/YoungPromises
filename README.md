# 🌟 Proyecto Jóvenes Promesas

## 📝 Descripción

Esta es una aplicación diseñada para que jugadores en formación puedan subir su información personal, deportiva y de contacto, con el fin de ser visibles para ojeadores, clubes y agentes de diferentes partes del mundo.

---

## 🏗️ Arquitectura de la Aplicación

El proyecto está estructurado bajo una **arquitectura por capas** (Layered Architecture), lo que permite una mejor separación de responsabilidades, escalabilidad y facilidad de mantenimiento.

### 📦 Estructura de proyectos

- **`YoungPromises.Api`**  
  Proyecto principal de la API desarrollado con .NET 9. Contiene los controladores, middlewares y configuración general. Expone los endpoints HTTP para ser consumidos por el frontend.

- **`YoungPromises.Service`**  
  Contiene la lógica de negocio, DTOs, enumeraciones y modelos de request/response. Sirve de capa intermedia entre la API y la base de datos.

- **`YoungPromises.Data`**  
  Responsable del acceso a datos, utilizando Entity Framework Core. Incluye el `DbContext`, entidades y repositorios.

- **`YoungPromises.Front`**  
  Proyecto frontend desarrollado en **Angular**, encargado de consumir los servicios expuestos por la API y presentar la información al usuario final.

---

### 🔁 Dependencias entre capas

- `Api` → depende de `Service` (para ejecutar lógica de negocio).
- `Service` → define contratos (interfaces) y lógica de negocio.
- `Data` → implementa interfaces de `Service` usando EF Core.
- `Front` → consume `Api` vía HTTP (sin referencias directas).

---

## 🛠️ Tecnologías utilizadas

- **Backend:** .NET 9 (ASP.NET Core)
- **ORM:** Entity Framework Core
- **Base de datos:** MySQL o SQL Server *(en evaluación, según costos y compatibilidad)*
- **Frontend:** Angular

---

## 🚧 Estado del Proyecto

> 🔨 En desarrollo...

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o pull request para discutir cambios importantes antes de implementarlos.


## 📄 Licencia

Este proyecto está licenciado bajo la licencia **CC BY-NC 4.0**.  
Puedes usarlo, modificarlo y distribuirlo siempre que no sea con fines comerciales.  
Más información: [https://creativecommons.org/licenses/by-nc/4.0/](https://creativecommons.org/licenses/by-nc/4.0/)
