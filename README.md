# YURES Docs

Repositorio autónomo de documentación de **YURES** construido con **MkDocs Material**.

Aquí se mantiene la guía por paneles:
- **Panel administrativo**
- **Panel operativo**

La documentación vive en `docs/`, la navegación se configura en `mkdocs.yml` y
`documentation/inventory.yml` registra la cobertura de las páginas publicadas.

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
mkdocs serve --dev-addr 0.0.0.0:8000
```

Luego abre en tu navegador desde este equipo:

- http://127.0.0.1:8000

Desde otro equipo de la misma red, reemplaza `<IP_LOCAL>` por la dirección IP
del equipo que ejecuta MkDocs:

- `http://<IP_LOCAL>:8000`

El servidor de desarrollo queda expuesto a la red local. No debe publicarse
directamente en Internet.

## Build de validación

```bash
mkdocs build --strict --clean
```

## Publicación

El manual publicado está en <https://yures.puyu.pe/storage/manual/>. Se sirve
mediante el enlace simbólico Laravel `public/storage` y el workflow no modifica
YURES, Apache ni el vhost.

La publicación se ejecuta automáticamente con cada push a `main`. También se
puede ejecutar manualmente desde **Actions** mediante el workflow **Publicar
manual**. El workflow construye el sitio y sincroniza `site/` con la ruta
completa de producción:

```text
/var/www/vhosts/yures.puyu.pe/httpdocs/app-prod/storage/app/public/manual/
```

Configura estos secrets en el Environment de GitHub `production`:

| Secret | Contenido |
| --- | --- |
| `DEPLOY_HOST` | Host SSH de producción. |
| `DEPLOY_USER` | Usuario SSH con acceso al directorio del manual. |
| `DEPLOY_SSH_PRIVATE_KEY` | Clave privada SSH de despliegue. |
| `DEPLOY_KNOWN_HOSTS` | Entrada `known_hosts` verificada del host SSH. |

El workflow usa SSH por el puerto 22 con verificación estricta del host. Para
revertir, ejecútalo manualmente sobre el commit anterior que contenía el manual
correcto; `rsync --delete` deja el destino exactamente como ese build.
