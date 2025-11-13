# Plataforma de Gestión Laboral

## 📋 Descripción

Plataforma web para gestión de citas, cálculos laborales y consultas. Versión neutral sin branding corporativo.

## 🚀 Implementación en GitHub

### Paso 1: Crear Repositorio en GitHub

1. Ve a [GitHub.com](https://github.com)
2. Haz clic en el botón **"New"** (esquina superior derecha, junto a tu foto de perfil)
3. Rellena los datos:
   - **Repository name**: `gestion-laboral` (o el nombre que prefieras)
   - **Description**: "Plataforma de gestión laboral"
   - Marca como **Public** o **Private** según prefieras
   - ✅ Marca **"Add a README file"**
4. Haz clic en **"Create repository"**

### Paso 2: Subir el Archivo HTML

Hay dos formas de hacerlo:

#### Opción A: Desde la interfaz web de GitHub (más fácil)

1. En tu repositorio recién creado, haz clic en **"Add file"** > **"Upload files"**
2. Arrastra el archivo `index.html` que te he creado
3. Escribe un mensaje de commit: "Añadir archivo principal"
4. Haz clic en **"Commit changes"**

#### Opción B: Usando Git desde tu ordenador (más profesional)

```bash
# 1. Clona el repositorio (reemplaza USERNAME y REPO con tus datos)
git clone https://github.com/USERNAME/gestion-laboral.git

# 2. Entra en la carpeta
cd gestion-laboral

# 3. Copia el archivo index.html a esta carpeta

# 4. Añade el archivo
git add index.html

# 5. Haz commit
git commit -m "Añadir archivo principal"

# 6. Sube los cambios
git push origin main
```

### Paso 3: Activar GitHub Pages

1. En tu repositorio, ve a **Settings** (configuración)
2. En el menú lateral izquierdo, busca **"Pages"**
3. En **"Source"**, selecciona **"Deploy from a branch"**
4. En **"Branch"**, selecciona:
   - Branch: `main`
   - Folder: `/ (root)`
5. Haz clic en **"Save"**
6. Espera 1-2 minutos

Tu página estará disponible en:
```
https://TU-USUARIO.github.io/gestion-laboral/
```

### Paso 4: Configurar Firebase (Opcional)

Si quieres usar la funcionalidad de base de datos:

1. Ve a [Firebase Console](https://console.firebase.google.com/)
2. Crea un nuevo proyecto
3. Añade una aplicación web
4. Copia la configuración de Firebase
5. En el archivo `index.html`, busca la línea 32:
   ```javascript
   const firebaseConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : {};
   ```
6. Reemplázala por:
   ```javascript
   const firebaseConfig = {
     apiKey: "TU_API_KEY",
     authDomain: "TU_AUTH_DOMAIN",
     projectId: "TU_PROJECT_ID",
     storageBucket: "TU_STORAGE_BUCKET",
     messagingSenderId: "TU_MESSAGING_SENDER_ID",
     appId: "TU_APP_ID"
   };
   ```

## 📁 Estructura del Proyecto

```
gestion-laboral/
│
├── index.html          # Archivo principal (único necesario)
├── README.md          # Este archivo
└── .gitignore         # (opcional) para ignorar archivos
```

## 🎨 Personalización

### Cambiar Colores

En el archivo `index.html`, busca estas líneas (aprox. línea 53-54):

```javascript
const PRIMARY_COLOR = '#2563eb'; // Azul - cámbialo por el color que quieras
const SECONDARY_COLOR = '#4B5563'; // Gris
```

Colores recomendados:
- Azul: `#2563eb`
- Verde: `#10b981`
- Morado: `#8b5cf6`
- Rojo: `#ef4444`

### Cambiar Teléfonos de Contacto

Busca las líneas (aprox. línea 55-56):

```javascript
const CONTACT_PHONE_1 = '34600000001';
const CONTACT_PHONE_2 = '34600000002';
```

Reemplaza con tus números reales (con prefijo internacional).

### Cambiar Textos

Todos los textos están en español y se pueden modificar directamente en el HTML. Busca las secciones que quieras cambiar y edita el texto.

## 🔧 Funcionalidades Incluidas

- ✅ **Sistema de Citas**: Reserva de citas con calendario interactivo
- ✅ **Calculadora de Nóminas**: Placeholder para cálculos salariales
- ✅ **Generador de Escritos**: Placeholder para documentos legales
- ✅ **FAQ**: Placeholder para preguntas frecuentes
- ✅ **PRL**: Placeholder para prevención de riesgos
- ✅ **Contacto**: Información de contacto

## 🆘 Solución de Problemas

### La página no se ve correctamente

1. Verifica que el archivo se llama exactamente `index.html`
2. Espera unos minutos para que GitHub Pages lo procese
3. Limpia la caché del navegador (Ctrl + F5)

### Firebase no funciona

1. Verifica que has configurado correctamente las credenciales
2. Asegúrate de que has activado Authentication en Firebase
3. Configura las reglas de Firestore

### Los estilos no cargan

El proyecto usa Tailwind CSS desde CDN, asegúrate de tener conexión a internet.

## 📝 Notas Importantes

1. **Sin Node.js requerido**: Este proyecto funciona directamente en el navegador
2. **Sin compilación**: No necesitas ningún proceso de build
3. **Responsive**: Funciona en móvil, tablet y escritorio
4. **Firebase Opcional**: La app funciona sin Firebase, pero sin persistencia de datos

## 🔄 Actualizar el Código

Si haces cambios en el archivo:

1. Guarda los cambios en `index.html`
2. Sube el archivo actualizado a GitHub (repite el Paso 2)
3. GitHub Pages se actualizará automáticamente en 1-2 minutos

## 📧 Soporte

Si tienes problemas:
1. Revisa que todos los pasos están completados
2. Verifica en la consola del navegador (F12) si hay errores
3. Comprueba que la URL de GitHub Pages es correcta

---

## 🎯 Próximos Pasos Recomendados

1. **Personalizar colores y textos** según tus necesidades
2. **Configurar Firebase** si quieres persistencia de datos
3. **Añadir un dominio personalizado** (opcional) en GitHub Pages
4. **Implementar las funcionalidades** de las páginas placeholder

## 📄 Licencia

Este proyecto es de código abierto y puede ser usado libremente.
