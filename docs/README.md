# 📚 Documentación

Este directorio contiene la documentación del proyecto Nearshore Connection - App de Contactos.

## Estructura de Carpetas

```
docs/
├── README.md                    # Este archivo
├── user-guides/                 # Guías de usuario
├── technical/                   # Documentación técnica
├── api/                         # Documentación de API
└── meeting-notes/              # Notas de reuniones
```

## Tipos de Documentos Soportados

Puedes subir los siguientes tipos de documentos:

### Documentos de Word
- **Formatos**: `.doc`, `.docx`
- **Uso**: Guías de usuario, especificaciones, documentación general
- **Ubicación recomendada**: `docs/user-guides/` o `docs/technical/`

### Hojas de Cálculo
- **Formatos**: `.xls`, `.xlsx`, `.csv`
- **Google Sheets**: Exporta como `.xlsx` o `.csv` antes de subir
- **Uso**: Datos de ejemplo, plantillas, especificaciones de campos
- **Ubicación recomendada**: `docs/technical/`

### Archivos PDF
- **Formatos**: `.pdf`
- **Uso**: Versiones finales de documentos, presentaciones exportadas
- **Ubicación recomendada**: Cualquier subcarpeta de `docs/`

### Archivos de Texto
- **Formatos**: `.md` (Markdown), `.txt`
- **Uso**: Documentación técnica, notas, cambios
- **Ubicación recomendada**: Cualquier subcarpeta de `docs/`

## Cómo Subir Documentos

### Opción 1: Interfaz Web de GitHub
1. Navega a la carpeta deseada en GitHub
2. Haz clic en "Add file" → "Upload files"
3. Arrastra tus archivos o haz clic para seleccionarlos
4. Escribe un mensaje de commit descriptivo
5. Haz clic en "Commit changes"

### Opción 2: Git Command Line
```bash
# 1. Copia tus archivos a la carpeta correspondiente
cp /ruta/a/tu/documento.docx docs/user-guides/

# 2. Agregar los archivos al staging
git add docs/

# 3. Hacer commit
git commit -m "Agregar documentación de usuario"

# 4. Subir cambios
git push
```

### Opción 3: GitHub Desktop
1. Copia tus archivos a la carpeta del proyecto
2. GitHub Desktop detectará automáticamente los cambios
3. Escribe un mensaje de commit
4. Haz clic en "Commit to main"
5. Haz clic en "Push origin"

## Google Sheets

Para subir hojas de Google Sheets:

1. **Método 1 - Exportar como archivo**:
   - Abre tu Google Sheet
   - Ve a Archivo → Descargar → Microsoft Excel (.xlsx)
   - Sube el archivo descargado a `docs/`

2. **Método 2 - Compartir link**:
   - Crea un archivo `google-sheets-links.md` en `docs/`
   - Agrega links a tus hojas de Google Sheets
   - Ejemplo:
     ```markdown
     ## Hojas de Cálculo del Proyecto
     
     - [Datos de Contactos](https://docs.google.com/spreadsheets/d/ID-DE-TU-SHEET)
     - [Configuración](https://docs.google.com/spreadsheets/d/ID-DE-TU-SHEET)
     ```

## Buenas Prácticas

✅ **Hacer**:
- Usar nombres de archivo descriptivos
- Organizar documentos en subcarpetas apropiadas
- Incluir fechas en nombres de versiones (ej: `manual-usuario-2026-01.docx`)
- Escribir mensajes de commit claros
- Mantener documentos actualizados

❌ **Evitar**:
- Subir archivos muy grandes (>10MB)
- Usar espacios en nombres de archivo (usa guiones: `mi-documento.docx`)
- Subir información sensible o credenciales
- Duplicar documentos sin versionado

## Límites de Tamaño

- **Archivos individuales**: Máximo 100MB (GitHub)
- **Recomendado**: Menos de 10MB por archivo
- **Archivos grandes**: Considera usar Git LFS o almacenamiento externo

## Versionado de Documentos

Para mantener versiones de documentos:

1. **Opción 1 - Git Nativo**:
   - Git mantiene automáticamente el historial
   - Accede a versiones antiguas desde el historial de commits

2. **Opción 2 - Nomenclatura**:
   - Incluye versión en el nombre: `manual-v1.0.docx`
   - Incluye fecha: `especificaciones-2026-01.docx`

## Soporte

¿Necesitas ayuda? Consulta:
- [README principal](../README.md)
- [Guía de contribución](../CONTRIBUTING.md)
- Contacta al administrador del proyecto
