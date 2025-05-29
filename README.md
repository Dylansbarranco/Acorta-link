# TAREA DE PROGRAMACIÓN EN C#

## 🎯 Tema: Desarrollo de un Acortador de URLs

---

## 🧠 Objetivo

Diseñar y desarrollar una aplicación en C# que permita a los usuarios ingresar una URL larga, generar un código corto único y recuperar posteriormente la URL original a partir del código generado. Esta tarea busca aplicar los fundamentos de la programación orientada a objetos, el uso de estructuras de datos y la manipulación de cadenas.

---

## 1. 📋 Enunciado

Desarrolla una aplicación en C# que funcione como un acortador de URLs. La aplicación debe permitir:

- Ingresar una URL larga.
- Generar un código corto alfanumérico que represente esa URL.
- Almacenar la relación entre el código y la URL.
- Recuperar la URL original mediante el código corto.

**La aplicación puede realizarse en consola o como una aplicación web sencilla utilizando ASP.NET Core.**

---

## 2. ⚙️ Detalles del desarrollo

El acortador de URL será una herramienta que permita simular el funcionamiento de servicios como Bit.ly o TinyURL de forma local.

### 🧩 Pasos sugeridos para el desarrollo (versión consola)

1. **Crear la clase `UrlShortener`:**

   - Método para generar un código corto (puedes usar parte de un GUID, timestamp o una cadena aleatoria).
   - Método para registrar una nueva URL.
   - Método para recuperar una URL original a partir de un código.

2. **Crear la clase `UrlRepository`:**

   - Utilizar un `Dictionary<string, string>` para almacenar las relaciones código-URL.
   - Métodos: `GuardarUrl(string code, string url)` y `ObtenerUrl(string code)`.

3. **Interacción desde consola en `Program.cs`:**

   - Menú de opciones para el usuario:
     1. Acortar una nueva URL.
     2. Recuperar una URL por su código.
     3. Ver todos los enlaces (opcional).
     4. Salir del programa.

4. **Validaciones:**

   - Comprobar que la URL ingresada es válida.
   - Evitar colisiones en los códigos generados (dos URLs diferentes no deben compartir código).

---

### 💻 Ejemplo de ejecución esperada:

- ienvenido al acortador de URLs

- Acortar nueva URL

- Recuperar URL

- Ver todos los enlaces

- Salir
- Seleccione una opción: 1
- Ingrese la URL: https://www.ejemplo.com/mi-enlace-super-largo
- Código generado: XyZ123

- Seleccione una opción: 2
- Ingrese el código corto: XyZ123
- URL original: https://www.ejemplo.com/mi-enlace-super-largo

  
---

### 🧠 Tips:

- Puedes crear un método estático `GenerarCodigo()` que devuelva una cadena de 6 caracteres aleatorios (letras y números).
- Si deseas ampliar el proyecto, guarda los datos en un archivo `.txt` o `.json` para mantenerlos entre ejecuciones.

---

## 🌐 Opcional (si dominas ASP.NET Core)

- Implementar el mismo sistema como una API REST con rutas POST y GET.
- Usar Entity Framework para guardar los datos en una base de datos SQLite.

---

## 3. 🗂️ Estructura sugerida del proyecto (Consola)

AcortadorUrls/
├── Program.cs // Interfaz principal del programa
├── UrlShortener.cs // Lógica para generar y manejar los códigos
├── UrlRepository.cs // Almacenamiento de la relación código - URL


## 👨‍💻 Autor

**Nombre:** Dilan Barranco (DilanDev)  
-Programación en C#  
**Descripción del trabajo:** Desarrollo de acortador de URLs en consola  


