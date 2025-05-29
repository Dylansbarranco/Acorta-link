# ACORTADOR DE URLS EN C#

## 🧠 Descripción del proyecto

Este proyecto es una aplicación de consola desarrollada en C# que simula el funcionamiento básico de un acortador de URLs (como Bit.ly o TinyURL). Permite:

- Acortar URLs largas generando un código único.
- Almacenar la relación entre código y URL original.
- Recuperar la URL original mediante el código corto.
- (Opcional) Ver todos los enlaces registrados.

---

## 📁 Estructura del proyecto

AcortadorUrls/
├── Program.cs // Interfaz de usuario y menú principal

├── UrlShortener.cs // Lógica para generar códigos cortos aleatorios

├── UrlRepository.cs // Diccionario para almacenar código-URL

├── LEEME.txt // Este archivo de instrucciones

├── AcortadorUrls.csproj // Archivo de configuración del proyecto

yaml
Copiar
Editar

---

## ⚙️ Cómo ejecutar

1. Abre el proyecto en Visual Studio Code o Visual Studio.
2. Asegúrate de tener el SDK de .NET instalado.
3. Ejecuta el programa con:

dotnet run

yaml
Copiar
Editar

---

## 🎮 Funcionalidad

### Menú principal:
Bienvenido al acortador de URLs

Acortar nueva URL

Recuperar URL

Ver todos los enlaces

Salir

yaml
Copiar
Editar

---

## 🔒 Validaciones y consideraciones

- Se generan códigos aleatorios de 6 caracteres (letras y números).
- Los datos no se guardan al cerrar el programa (no hay persistencia en archivos aún).
- Se evita colisión de códigos (se puede mejorar más adelante).
- Este proyecto es 100% educativo y puede evolucionarse a una API con ASP.NET.

---

## 👨‍💻 Autor

Desarrollado por: DilanDev  
Materia: Programación en C#  
Proyecto: Tarea de acortador de URLs  

---

## 🧪 Mejoras futuras

- Persistencia de datos en archivo `.json` o `.txt`
- Interfaz web con ASP.NET Core
- API REST con Entity Framework y SQLite

---
