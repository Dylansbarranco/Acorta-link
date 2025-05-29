# 🔗 Acortador de URLs con ASP.NET Core y Firebase

## 🎯 Objetivo

Desarrollar una API REST en C# usando ASP.NET Core que permita:
- Acortar URLs largas.
- Generar códigos únicos y cortos.
- Recuperar la URL original mediante el código.
- Almacenar los datos en Firebase (Cloud Firestore).

---

## 📁 Estructura del Proyecto

```
AcortadorUrls/
├── Controllers/
│   └── UrlController.cs         # Controlador de rutas de la API
├── Models/
│   └── UrlEntry.cs              # Modelo de datos para URL y código
├── Repositories/
│   └── UrlRepository.cs         # Acceso a Firestore
├── Services/
│   └── UrlShortenerService.cs   # Lógica de generación de códigos y acortador
├── appsettings.json             # Configuración de Firebase
├── Program.cs                   # Configuración y arranque del proyecto
├── AcortadorUrls.csproj         # Archivo de proyecto .NET
├── AcortadorUrls.sln            # Solución del proyecto
├── README.md                    # Este documento
```

---

## 🔥 Integración con Firebase

1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/).
2. Activa **Cloud Firestore**.
3. Crea una cuenta de servicio:
   - Ve a Configuración del Proyecto > Cuentas de servicio.
   - Genera una nueva clave privada y guárdala como `serviceAccountKey.json`.
   - Colócala en la raíz o en una carpeta `/firebase` (añádela al `.gitignore`).
4. Instala el SDK de Firestore:
   ```bash
   dotnet add package Google.Cloud.Firestore
   ```

---

## 🚀 Endpoints principales

- **POST `/api/url`**  
  Envía una URL larga y recibe un código corto.

- **GET `/api/url/{code}`**  
  Recupera la URL original a partir del código.

---

## 🛠️ Ejemplo de uso

**POST /api/url**

```json
{
  "originalUrl": "https://www.ejemplo.com/super-largo"
}
```
**Respuesta:**
```json
{
  "shortCode": "XyZ123"
}
```

**GET /api/url/XyZ123**

**Respuesta:**
```json
{
  "originalUrl": "https://www.ejemplo.com/super-largo"
}
```

---

## ✅ Validaciones

- Validación de formato de URL.
- Prevención de colisiones de códigos cortos.
- Persistencia en Firestore.

---


## 👨‍💻 Autor

- **Dilan Barranco**

## 📌 Proyecto

- **Acorta Link con C# y Base de Datos (Firebase Firestore)**
- Proyecto educativo para aprender sobre APIs REST, ASP.NET Core y la integración con bases de datos NoSQL en la nube.
