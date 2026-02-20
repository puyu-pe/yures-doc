# YURES Docs

Repositorio de documentación de **YURES** construido con **MkDocs Material**.

Aquí se mantiene la guía por paneles:
- **Panel administrativo**
- **Panel operativo**

La documentación vive en la carpeta `docs/` y la navegación se configura en `mkdocs.yml`.

## Levantar localmente

### 1) Crear y activar entorno virtual

```bash
python -m venv .venv
source .venv/bin/activate
```

### 2) Instalar dependencias

```bash
pip install -r requirements.txt
```

### 3) Ejecutar servidor local

```bash
mkdocs serve
```

Luego abre en tu navegador:

- http://127.0.0.1:8000

## Build de validación

```bash
mkdocs build
```
