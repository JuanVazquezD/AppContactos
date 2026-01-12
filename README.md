📇 Nearshore Connection - App de Contactos
Sistema de gestión de contactos para eventos de Nearshore Connection.
📋 Descripción
Esta webapp permite:
✅ Gestionar un directorio de Contactos y Organizaciones
✅ Vista jerárquica (Organizaciones → Contactos)
✅ Formularios de alta y edición
✅ Sistema de búsqueda global
✅ Backend conectado a Google Sheets
✅ Log de cambios automático
✅ Sistema de permisos por usuario
🗂️ Estructura de Archivos
nearshore-contacts/
├── index.html      # Frontend principal (HTML/CSS/JS)
├── Code.gs         # Backend Google Apps Script
└── README.md       # Este archivo
🚀 Instalación
Paso 1: Configurar Google Sheets
Tu Google Sheet ya tiene el ID: 1FYEiUzBITwjcEgfQKlDD6tLDO8UFvxz-kKyaGHq8Jt4
Asegúrate de tener las siguientes pestañas:
Contactos
Organizaciones
Opciones
Permisos
Panel Administración
Campos
Staff
Comentarios
Log Cambios
Paso 2: Instalar Google Apps Script
Abre tu Google Sheet
Ve a Extensiones → Apps Script
Elimina el código existente
Copia y pega todo el contenido de Code.gs
Guarda el proyecto (Ctrl+S o Cmd+S)
Ejecuta la función initializeSheets() una vez para crear la estructura
Paso 3: Desplegar como Aplicación Web
En Apps Script, haz clic en Implementar → Nueva implementación
Selecciona tipo: Aplicación web
Configuración:
Descripción: "Nearshore Contacts API v1"
Ejecutar como: "Yo"
Quién tiene acceso: "Cualquier persona"
Haz clic en Implementar
Copia la URL de la aplicación web
Paso 4: Conectar Frontend con Backend
Abre index.html
Busca la sección CONFIG (línea ~1650 aprox.)
Reemplaza:
const CONFIG = {
    SHEET_ID: '1FYEiUzBITwjcEgfQKlDD6tLDO8UFvxz-kKyaGHq8Jt4',
    API_URL: 'TU_URL_DE_APPS_SCRIPT_AQUÍ',  // ← Pega tu URL aquí
    DEMO_MODE: false  // ← Cambiar a false
};
Paso 5: Publicar el Frontend
Tienes varias opciones:
Opción A: GitHub Pages (Gratis)
Crea un repositorio en GitHub
Sube index.html
Ve a Settings → Pages → Activa GitHub Pages
Tu app estará en https://tuusuario.github.io/nearshore-contacts/
Opción B: Netlify (Gratis)
Ve a netlify.com
Arrastra y suelta la carpeta
Obtén tu URL automáticamente
Opción C: Google Sites
Crea un sitio en Google Sites
Añade un bloque "Insertar" → "Insertar código"
Pega el contenido HTML
Opción D: Servidor propio
Sube index.html a tu servidor web
Accede vía tu dominio
📊 Estructura de Datos
Pestaña: Contactos
Columna
Descripción
Contacto ID
Identificador único (auto-generado)
Directorio
Categoría del directorio
Organización
Referencia a Organizaciones
Nombre
Nombre completo
Puesto
Cargo o posición
Celular
Número de celular
Email
Correo electrónico
Activo
✅ o ❌
Estatus
Estado del contacto
Pestaña: Organizaciones
Columna
Descripción
ID Organización
Identificador único
Tipo Organización
Empresa, Gobierno, Academia, etc.
Sector
Industria o sector
Tier
Nivel (Tier 1, 2, 3)
Nombre
Nombre de la organización
Ubicación
Ciudad, Estado
Página Web
URL del sitio web
🔧 Personalización
Cambiar Colores
En index.html, busca :root y modifica las variables CSS:
:root {
    --primary: #0D4F8B;        /* Color principal */
    --accent: #E8A838;         /* Color de acento */
    --bg-sidebar: #0A3A5C;     /* Fondo sidebar */
    /* ... más variables ... */
}
Agregar Opciones de Dropdown
Ve a la pestaña Opciones en Google Sheets
Agrega filas con el formato: Categoría | Valor
Ejemplo:
Sector | Manufactura
Sector | Tecnología
Tipo Organización | Empresa
Modificar Campos
Edita la pestaña Campos en Google Sheets para:
Agregar nuevos campos
Cambiar tipos de datos
Establecer campos obligatorios
🔐 Seguridad
Permisos
Los permisos se configuran en la pestaña Permisos:
Gestor: Lectura y escritura en Contactos/Organizaciones
Coordinador: Gestor + Opciones
Administrador: Coordinador + Staff/Permisos
Administrador Sistema: Acceso total
Autenticación
Para agregar login con Google:
En Apps Script, usa Session.getActiveUser().getEmail()
Valida contra la pestaña Staff
📝 API Reference
GET Endpoints
?action=getData         → Todos los datos
?action=getContacts     → Solo contactos
?action=getOrganizations → Solo organizaciones
?action=getOptions      → Opciones de dropdowns
POST Actions
// Guardar contacto
{ action: 'saveContact', data: {...} }

// Guardar organización
{ action: 'saveOrganization', data: {...} }

// Eliminar registro
{ action: 'delete', table: 'contacts', id: 'CON001' }
🐛 Solución de Problemas
Error: "No se pueden cargar los datos"
Verifica que la URL de Apps Script sea correcta
Asegúrate de que DEMO_MODE esté en false
Revisa los permisos de la aplicación web
Los cambios no se guardan
Verifica que tienes permisos de edición en el Sheet
Revisa la consola del navegador (F12)
Ejecuta testConnection() en Apps Script
Error de CORS
Si ves errores de CORS, asegúrate de:
Usar HTTPS en tu frontend
La app de Apps Script esté publicada como "Cualquier persona"
📞 Soporte
Para reportar problemas o solicitar funciones:
Revisa la documentación
Verifica la configuración
Contacta al administrador del sistema
📜 Licencia
Proyecto desarrollado para Nearshore Connection.
Uso interno - Todos los derechos reservados.
Versión: 1.0.0
Última actualización: Enero 2026
Desarrollado con: HTML, CSS, JavaScript, Google Apps Script
