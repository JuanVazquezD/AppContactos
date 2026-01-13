# Guía Rápida: Subir Documentos y Diseños

## ✅ Respuesta Rápida

**Sí, puedes subir:**
1. ✅ Documentos de Word (.docx, .doc)
2. ✅ Hojas de Google Sheets (exportadas o como enlaces)
3. ✅ Carpeta completa con diseños de Google Stitch

---

## 📄 1. Subir Documentos de Word

### Método Más Fácil (Web de GitHub):
1. Ve a: https://github.com/JuanVazquezD/AppContactos
2. Navega a la carpeta `docs/`
3. Haz clic en **"Add file"** → **"Upload files"**
4. Arrastra tus archivos `.docx`
5. Escribe un mensaje: "Agregar [nombre del documento]"
6. Haz clic en **"Commit changes"**

### ¿Dónde Subir?
- Manuales de usuario → `docs/user-guides/`
- Documentación técnica → `docs/technical/`
- Notas de reuniones → `docs/meeting-notes/`

---

## 📊 2. Subir Google Sheets

### Opción A: Exportar y Subir
```
1. Abre tu Google Sheet
2. Archivo → Descargar → Microsoft Excel (.xlsx)
3. Sube el archivo .xlsx a docs/technical/
4. Nombra descriptivamente: "configuracion-2026-01.xlsx"
```

### Opción B: Compartir Enlaces (Recomendado ⭐)
```
1. Abre el archivo: docs/google-sheets-links.md
2. Agrega tu enlace:

### [Nombre de tu Hoja](https://docs.google.com/spreadsheets/d/TU-ID-AQUI)
- Descripción: Para qué sirve
- Actualizada: 2026-01-13
- Responsable: Tu nombre

3. Guarda el archivo
4. Haz commit y push
```

**Ventajas de usar enlaces:**
- ✅ Cambios en tiempo real
- ✅ No duplicas datos
- ✅ Colaboración inmediata
- ✅ No ocupa espacio

---

## 🎨 3. Subir Carpeta con Diseños de Google Stitch

### Método Más Fácil (GitHub Desktop):

#### Paso 1: Descargar GitHub Desktop
- Ve a: https://desktop.github.com/
- Descarga e instala

#### Paso 2: Clonar el Repositorio
```
1. Abre GitHub Desktop
2. File → Clone Repository
3. Busca: JuanVazquezD/AppContactos
4. Selecciona una ubicación en tu computadora
5. Haz clic en "Clone"
```

#### Paso 3: Copiar tus Diseños
```
1. Ve a la carpeta del repositorio en tu computadora
2. Abre la carpeta: designs/google-stitch/
3. Copia toda tu carpeta de diseños aquí
4. Organiza en subcarpetas:
   - wireframes/ (bocetos)
   - mockups/ (diseños finales)
   - prototypes/ (prototipos)
```

#### Paso 4: Subir a GitHub
```
1. GitHub Desktop mostrará todos los archivos nuevos
2. En el campo de mensaje escribe: "Agregar diseños de Google Stitch"
3. Haz clic en "Commit to copilot/add-document-upload-functionality"
4. Haz clic en "Push origin"
```

### Método Alternativo (Línea de Comandos):
```bash
# 1. Clona el repositorio
git clone https://github.com/JuanVazquezD/AppContactos.git
cd AppContactos

# 2. Copia tu carpeta de diseños
cp -r /ruta/a/tus/diseños/* designs/google-stitch/

# 3. Agrega y sube
git add designs/
git commit -m "Agregar diseños de Google Stitch"
git push
```

---

## 📁 Estructura de Carpetas Creada

```
AppContactos/
├── docs/                    ← DOCUMENTOS AQUÍ
│   ├── user-guides/        ← Manuales .docx
│   ├── technical/          ← Google Sheets exportados
│   ├── api/
│   ├── meeting-notes/
│   └── google-sheets-links.md  ← Enlaces a Google Sheets
│
└── designs/                 ← DISEÑOS AQUÍ
    └── google-stitch/      ← TU CARPETA DE DISEÑOS
        ├── wireframes/
        ├── mockups/
        └── prototypes/
```

---

## 🎯 Resumen Ultra-Rápido

| Qué Subir | Dónde | Método Más Fácil |
|-----------|-------|------------------|
| Word (.docx) | `docs/` | GitHub web: Add file → Upload files |
| Google Sheets | `docs/google-sheets-links.md` | Agregar enlace (no exportar) |
| Carpeta de Diseños | `designs/google-stitch/` | GitHub Desktop |

---

## 💡 Tips

1. **Word**: Usa nombres descriptivos sin espacios
   - ✅ `manual-usuario-v1.docx`
   - ❌ `Manual Usuario Final.docx`

2. **Google Sheets**: Mejor compartir enlaces que exportar
   - Mantiene sincronización
   - Colaboración en tiempo real

3. **Diseños**: Organiza en subcarpetas
   - `wireframes/` para bocetos
   - `mockups/` para diseños finales

---

## 📚 Documentación Completa

Para más detalles, consulta:
- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Guía completa paso a paso
- **[docs/README.md](docs/README.md)** - Todo sobre documentos
- **[designs/README.md](designs/README.md)** - Todo sobre diseños

---

## 🆘 ¿Necesitas Ayuda?

1. Lee esta guía primero
2. Consulta [CONTRIBUTING.md](CONTRIBUTING.md)
3. Abre un Issue en GitHub
4. Contacta al administrador del proyecto
