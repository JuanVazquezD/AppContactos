# Guía de Contribución

¡Gracias por contribuir al proyecto Nearshore Connection - App de Contactos! Esta guía te ayudará a subir documentos, diseños y código de manera efectiva.

## 📋 Tabla de Contenidos

- [Cómo Subir Documentos](#cómo-subir-documentos)
- [Cómo Subir Diseños](#cómo-subir-diseños)
- [Cómo Contribuir con Código](#cómo-contribuir-con-código)
- [Buenas Prácticas](#buenas-prácticas)

## 📄 Cómo Subir Documentos

### Documentos de Word

Sí, **puedes subir documentos de Word** (`.doc`, `.docx`) al repositorio.

**Pasos:**

1. **Ubicación**: Coloca tus documentos en la carpeta `docs/`
   - Guías de usuario → `docs/user-guides/`
   - Documentación técnica → `docs/technical/`
   - Notas de reuniones → `docs/meeting-notes/`

2. **Método Recomendado - GitHub Web**:
   ```
   1. Ve a https://github.com/JuanVazquezD/AppContactos
   2. Navega a la carpeta docs/
   3. Haz clic en "Add file" → "Upload files"
   4. Arrastra tus archivos .docx
   5. Escribe: "Agregar [nombre del documento]"
   6. Haz clic en "Commit changes"
   ```

3. **Método Alternativo - Git Command Line**:
   ```bash
   git clone https://github.com/JuanVazquezD/AppContactos.git
   cd AppContactos
   cp /ruta/a/tu/documento.docx docs/user-guides/
   git add docs/
   git commit -m "Agregar guía de usuario"
   git push
   ```

### Hojas de Google Sheets

Sí, **puedes compartir hojas de Google Sheets** de dos formas:

#### Opción 1: Exportar y Subir
```
1. Abre tu Google Sheet
2. Archivo → Descargar → Microsoft Excel (.xlsx)
3. Sube el archivo .xlsx a docs/technical/
4. Nombra el archivo descriptivamente: "configuracion-campos-2026-01.xlsx"
```

#### Opción 2: Compartir Links (Recomendado)
```
1. Crea un archivo llamado "google-sheets-links.md" en docs/
2. Agrega tus links de Google Sheets:

## Hojas de Cálculo del Proyecto

- [Configuración de Campos](https://docs.google.com/spreadsheets/d/TU-ID-AQUI)
- [Datos de Prueba](https://docs.google.com/spreadsheets/d/TU-ID-AQUI)
- [Plantilla de Contactos](https://docs.google.com/spreadsheets/d/TU-ID-AQUI)

3. Asegúrate de que los permisos de la hoja permitan acceso
4. Sube el archivo .md a GitHub
```

**Ventajas de usar links**:
- Los cambios en Google Sheets se reflejan automáticamente
- No hay duplicación de datos
- Colaboración en tiempo real
- No ocupa espacio en el repositorio

## 🎨 Cómo Subir Diseños

### Diseños de Google Stitch

Sí, **puedes subir una carpeta completa con diseños de Google Stitch**.

**Pasos:**

1. **Exportar desde Google Stitch**:
   - Exporta cada diseño como PNG o JPG
   - Descarga todos los archivos a una carpeta local

2. **Organizar localmente**:
   ```
   mis-diseños/
   ├── wireframes/
   │   ├── login.png
   │   └── dashboard.png
   └── mockups/
       ├── login-final.png
       └── dashboard-final.png
   ```

3. **Método 1 - GitHub Desktop (Más Fácil)**:
   ```
   1. Descarga GitHub Desktop: https://desktop.github.com/
   2. Clona el repositorio en GitHub Desktop
   3. Copia tu carpeta de diseños a: AppContactos/designs/google-stitch/
   4. GitHub Desktop mostrará todos los archivos nuevos
   5. Escribe mensaje: "Agregar diseños de Google Stitch"
   6. Haz clic en "Commit to main"
   7. Haz clic en "Push origin"
   ```

4. **Método 2 - Git Command Line**:
   ```bash
   # Clona el repositorio si no lo tienes
   git clone https://github.com/JuanVazquezD/AppContactos.git
   cd AppContactos
   
   # Copia tu carpeta de diseños completa
   cp -r /ruta/a/tus/diseños/* designs/google-stitch/
   
   # Agrega todos los archivos
   git add designs/
   
   # Verifica lo que vas a subir
   git status
   
   # Haz commit
   git commit -m "Agregar diseños de Google Stitch con wireframes y mockups"
   
   # Sube a GitHub
   git push
   ```

5. **Método 3 - Interfaz Web de GitHub**:
   ```
   GitHub no permite subir carpetas directamente, pero puedes:
   
   1. Ve a designs/google-stitch/wireframes/
   2. Haz clic en "Add file" → "Upload files"
   3. Arrastra TODOS los wireframes a la vez
   4. Haz commit
   5. Repite para cada subcarpeta (mockups, prototypes, etc.)
   ```

### Tipos de Archivos de Diseño Soportados

- ✅ Imágenes: PNG, JPG, SVG, GIF
- ✅ Archivos de diseño: Figma (.fig), Sketch (.sketch), Adobe XD (.xd)
- ✅ PDFs de presentaciones
- ✅ Prototipos exportados

## 💻 Cómo Contribuir con Código

### Cambios al Código

1. **Fork del repositorio**
2. **Crea una rama**:
   ```bash
   git checkout -b feature/mi-nueva-caracteristica
   ```
3. **Haz tus cambios**
4. **Commit**:
   ```bash
   git commit -m "Descripción clara del cambio"
   ```
5. **Push y crea Pull Request**

## ✅ Buenas Prácticas

### Nomenclatura de Archivos

**✅ Recomendado:**
```
manual-usuario-v1.0.docx
configuracion-campos-2026-01.xlsx
wireframe-login-v2.png
mockup-dashboard-final.png
```

**❌ Evitar:**
```
Manual de Usuario Final FINAL.docx  (confuso)
Captura de pantalla 2026-01-13.png  (espacios, no descriptivo)
diseño1.png                         (no descriptivo)
```

### Mensajes de Commit

**✅ Buenos mensajes:**
```
Agregar manual de usuario v1.0
Actualizar diseños de Google Stitch con nuevos mockups
Incluir hoja de cálculo de configuración de campos
```

**❌ Malos mensajes:**
```
Update
Cambios varios
asdf
```

### Organización de Archivos

```
AppContactos/
├── docs/                    # 📄 DOCUMENTOS AQUÍ
│   ├── user-guides/        # Manuales de usuario, guías
│   ├── technical/          # Especificaciones técnicas, hojas de cálculo
│   ├── api/                # Documentación de API
│   └── meeting-notes/      # Notas de reuniones
│
├── designs/                 # 🎨 DISEÑOS AQUÍ
│   ├── google-stitch/      # Tus diseños de Google Stitch
│   │   ├── wireframes/
│   │   ├── mockups/
│   │   └── prototypes/
│   ├── figma/              # Exportaciones de Figma
│   ├── screenshots/        # Capturas de pantalla
│   └── assets/             # Recursos gráficos
│       ├── icons/
│       ├── logos/
│       └── images/
│
├── index.html              # Código de la aplicación
├── CodigoGS                # Código de Google Apps Script
└── README.md               # Documentación principal
```

## 📏 Límites y Consideraciones

### Tamaños de Archivo

- **Documentos Word/Excel**: < 10MB recomendado
- **Imágenes de diseño**: < 5MB recomendado
- **Archivos de diseño**: < 20MB recomendado
- **Máximo por archivo en GitHub**: 100MB

### Si Tienes Archivos Muy Grandes

1. **Comprime imágenes**: Usa TinyPNG, ImageOptim
2. **Usa enlaces externos**: Google Drive, Dropbox
3. **Git LFS**: Para archivos > 50MB (requiere configuración)

## 🆘 Solución de Problemas

### "El archivo es muy grande"
→ Comprime el archivo o usa enlaces externos

### "No puedo subir una carpeta completa por web"
→ Usa GitHub Desktop o Git Command Line

### "No sé usar Git"
→ Usa GitHub Desktop (interfaz gráfica, muy fácil)

### "Necesito colaborar en tiempo real"
→ Mantén documentos en Google Drive/Sheets y comparte links

## 📞 ¿Necesitas Ayuda?

1. Revisa esta guía primero
2. Consulta [docs/README.md](docs/README.md) para documentos
3. Consulta [designs/README.md](designs/README.md) para diseños
4. Abre un Issue en GitHub
5. Contacta al administrador del proyecto

---

## Resumen Rápido

| Tipo | ¿Puedes Subirlo? | Dónde | Cómo |
|------|------------------|-------|------|
| Word (.docx) | ✅ Sí | `docs/` | GitHub web o Git |
| Google Sheets | ✅ Sí (exportado o link) | `docs/technical/` | Exportar como .xlsx o compartir link |
| Carpeta de Diseños | ✅ Sí | `designs/google-stitch/` | GitHub Desktop (recomendado) o Git |
| Imágenes PNG/JPG | ✅ Sí | `designs/` | GitHub web o Git |
| PDFs | ✅ Sí | `docs/` | GitHub web o Git |

**Método más fácil para carpetas completas: GitHub Desktop** 
→ https://desktop.github.com/
