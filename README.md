# create strucdb

Generador de proyectos Node.js con estructura base, ideal para comenzar rápidamente con Express.

## ⚠️ **Importante**
>Este proyecto necesita que **MongoDB esté instalado y ejecutándose** en tu sistema.

Puedes verificar que está corriendo ejecutando:

```bash
mongod
```
Esto levantará el servidor de MongoDB. Si ves mensajes indicando que está “listening on port 27017”, todo va bien.

Para entrar a la consola interactiva de MongoDB y hacer consultas, abre otra terminal y ejecuta:

```bash
mongosh
```
ℹ️ Si no tienes MongoDB instalado, descárgalo desde:  
👉 https://www.mongodb.com/try/download/community   
ℹ️ Si no quieres usar MongoDB localmente, usa Atlas:  
👉 https://cloud.mongodb.com  
-[¿Cómo usar MongoDB Atlas?]()
---

## 🛠 ¿Qué hace este generador?

Este paquete crea una estructura básica para un proyecto Node.js, incluyendo:

- Un archivo `index.js` configurado con Express
- Instalación automática de dependencias como `express`, `mongoose`, `path` y `open`.
- Carpetas `public/` y `private/` creadas automáticamente

## 📁 Estructura del proyecto

strucdb/  
├── index.js  
├── package.json  
├── package.lock.json  
├── node_modules/  
├── public/  
└── private/  

---

## 🤓 Explicacion de las carpetas `public/` y `private/`

### 📂 `public/`

Contiene las carpetas de pages,styles y js, mismas las cuales sirven para el Frontend del proyecto.
De igual manera contiene el index.html que es la primer pagina que se abre cuando el proyecto se ejecuta.

### 📁 Estructura del Frontend

public/  
├── pages/            # Páginas HTML públicas  
|   ├── styles/           # Hojas de estilo CSS  
|   └── js/               # Scripts del cliente (JavaScript del navegador)  
└── index.html    # Página principal

Express servirá esta carpeta automáticamente usando:

```js
app.use(express.static(path.join(__dirname, 'public')));
```
---

### 📂 `private/`

Contiene las carpetas de modules y routes junto con el archivo de conexion a MongoDB, estos mismos sirvan para el Backend del proyecto

### 📁 Estructura del Backend

private/  
├── Conexion.js           # Archivo que configura la conexión a la base de datos  
├── modules/              # Contiene la lógica de negocio (modelos, controladores, servicios)  
└── routes/               # Define las rutas de la API o servidor

Mongoose servirá para conectar MongoDB a tu proyecto.
[]

---
