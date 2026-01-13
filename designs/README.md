# 🎨 Diseños y Maquetas

Este directorio contiene todos los archivos de diseño del proyecto Nearshore Connection.

## Estructura de Carpetas

```
designs/
├── README.md                    # Este archivo
├── google-stitch/              # Diseños de Google Stitch
│   ├── wireframes/             # Wireframes de baja fidelidad
│   ├── mockups/                # Mockups de alta fidelidad
│   └── prototypes/             # Prototipos interactivos
├── figma/                      # Archivos de Figma (exportados)
├── assets/                     # Recursos gráficos
│   ├── icons/                  # Iconos
│   ├── logos/                  # Logos
│   └── images/                 # Imágenes
└── screenshots/                # Capturas de pantalla de la app
```

## Google Stitch

### ¿Qué es Google Stitch?

Google Stitch es una herramienta para crear mockups y diseños de interfaces de usuario.

### Cómo Subir Diseños de Google Stitch

1. **Exportar desde Google Stitch**:
   - Exporta tus diseños como imágenes PNG o JPG
   - O exporta el proyecto completo si es posible

2. **Organizar archivos**:
   ```
   designs/google-stitch/
   ├── wireframes/
   │   ├── login-screen.png
   │   ├── dashboard.png
   │   └── contacts-list.png
   ├── mockups/
   │   ├── login-final.png
   │   ├── dashboard-final.png
   │   └── contacts-list-final.png
   └── prototypes/
       └── app-flow.png
   ```

3. **Subir a GitHub**:
   - Arrastra los archivos a la carpeta correspondiente
   - Haz commit con un mensaje descriptivo

### Formatos Soportados

#### Imágenes
- **PNG**: Ideal para mockups y wireframes con transparencia
- **JPG/JPEG**: Para capturas de pantalla y mockups sin transparencia
- **SVG**: Para iconos y gráficos vectoriales
- **GIF**: Para animaciones simples

#### Archivos de Diseño
- **Figma**: Exporta como `.fig` o comparte el link
- **Adobe XD**: Exporta como `.xd`
- **Sketch**: Exporta como `.sketch`
- **PDF**: Para presentaciones de diseño

## Cómo Subir una Carpeta Completa

### Método 1: Interfaz Web de GitHub

GitHub no permite subir carpetas directamente desde la web, pero puedes:

1. **Crear la estructura de carpetas**:
   - Crea cada subcarpeta manualmente en GitHub
   - Usa "Add file" → "Create new file"
   - Nombra el archivo como `carpeta/subcarpeta/.gitkeep` para crear la estructura

2. **Subir archivos**:
   - Ve a cada carpeta
   - Usa "Add file" → "Upload files"
   - Sube los archivos correspondientes

### Método 2: Git Command Line (Recomendado)

```bash
# 1. Navega a tu repositorio local
cd /ruta/a/AppContactos

# 2. Copia toda tu carpeta de diseños
cp -r /ruta/a/tus/diseños/* designs/google-stitch/

# 3. Agrega todos los archivos
git add designs/

# 4. Verifica qué se va a subir
git status

# 5. Haz commit
git commit -m "Agregar diseños de Google Stitch"

# 6. Sube a GitHub
git push
```

### Método 3: GitHub Desktop

1. **Copiar archivos**:
   - Copia tu carpeta de diseños completa
   - Pégala en `designs/google-stitch/` en tu repositorio local

2. **Hacer commit**:
   - GitHub Desktop mostrará todos los archivos nuevos
   - Escribe un mensaje: "Agregar diseños de Google Stitch"
   - Haz clic en "Commit to main"

3. **Push**:
   - Haz clic en "Push origin"

## Nomenclatura de Archivos

### Buenas Prácticas

✅ **Recomendado**:
```
login-screen-v1.png
dashboard-wireframe-2026-01.png
contact-form-mockup-final.png
icon-user-24x24.svg
```

❌ **Evitar**:
```
Captura de pantalla 2026-01-13.png  (espacios)
diseño final final FINAL.png         (versionado confuso)
IMG_001.png                          (nombre no descriptivo)
```

### Convenciones de Nombres

- **Wireframes**: `[nombre-pantalla]-wireframe.png`
- **Mockups**: `[nombre-pantalla]-mockup.png`
- **Prototipos**: `[nombre-flujo]-prototype.png`
- **Iconos**: `icon-[nombre]-[tamaño].svg`
- **Screenshots**: `screenshot-[pantalla]-[fecha].png`

## Versiones de Diseño

Mantén un registro de versiones:

```
designs/google-stitch/
├── v1.0/
│   ├── login.png
│   └── dashboard.png
├── v1.1/
│   ├── login.png
│   └── dashboard.png
└── latest/         # Symlinks o copias de la versión actual
    ├── login.png
    └── dashboard.png
```

## Links a Herramientas de Diseño

Si prefieres no subir archivos grandes, puedes mantener links:

Crea un archivo `design-links.md`:

```markdown
## Enlaces a Diseños

### Figma
- [Diseño Principal](https://figma.com/file/...)
- [Sistema de Diseño](https://figma.com/file/...)

### Google Stitch
- [Mockups de App](https://stitch.google.com/...)
- [Wireframes](https://stitch.google.com/...)

### Adobe XD
- [Prototipo Interactivo](https://xd.adobe.com/...)
```

## Límites de Tamaño

- **Imágenes individuales**: Recomendado < 5MB
- **Archivos de diseño**: Recomendado < 20MB
- **Total del directorio**: Mantener bajo 100MB

### Para Archivos Grandes

Si tienes archivos muy grandes:

1. **Comprime imágenes**:
   - Usa herramientas como TinyPNG, ImageOptim
   - Reduce resolución si no es necesaria alta calidad

2. **Usa Git LFS** (Large File Storage):
   ```bash
   git lfs install
   git lfs track "*.psd"
   git lfs track "*.sketch"
   ```

3. **Almacenamiento externo**:
   - Google Drive
   - Dropbox
   - Mantén links en el repositorio

## Capturas de Pantalla

Para documentar el estado actual de la aplicación:

```bash
designs/screenshots/
├── 2026-01/
│   ├── login-screen.png
│   ├── dashboard.png
│   ├── contacts-list.png
│   └── organization-detail.png
└── 2026-02/
    └── ... (nuevas capturas)
```

## Soporte

¿Necesitas ayuda?
- Revisa el [README principal](../README.md)
- Consulta la [documentación](../docs/README.md)
- Contacta al equipo de diseño
