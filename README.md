
# Proyecto Base con FastAPI para Detección de Texto en PDFs e Imágenes

Este proyecto es una estructura base para una aplicación web desarrollada con **FastAPI**, organizada en módulos y con soporte para Docker y CI/CD. 

## Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

```
app/
    api/
    core/
    db/
    schemas/
    services/
    business/
migrations/
tests/
ci_cd/
docker/
main.py
```

### Carpetas principales:

- **`app/`**: Contiene la lógica de la aplicación, dividida en diferentes módulos como rutas (`api/`), configuración (`core/`), base de datos (`db/`), esquemas (`schemas/`) y servicios (`services/`).
- **`migrations/`**: Contiene los archivos de migración de base de datos (probablemente usando Alembic).
- **`tests/`**: Pruebas unitarias e integraciones de la aplicación.
- **`ci_cd/`**: Scripts y configuraciones para la integración y despliegue continuo.
- **`docker/`**: Configuraciones de Docker para los diferentes entornos (desarrollo, testing, producción).

## Requisitos Previos

- **Python 3.8+**
- **Docker** (opcional para entornos contenedorizados)
- **Poetry** o **pip** para la gestión de dependencias.

## Instalación y Configuración

### 1. Clonar el repositorio

Clona este repositorio en tu máquina local:

```bash
git clone <url-del-repositorio>
cd <nombre-del-proyecto>
```
### 2. Uso de Docker

Si deseas usar Docker para la ejecución del proyecto, hay tres entornos disponibles: desarrollo, testing, y producción. Para cada entorno puedes encontrar un `Dockerfile` y un archivo `docker-compose.yml` en el directorio `docker/`.

Ejemplo para desarrollo:

```bash
docker-compose -f docker/develop/docker-compose.yml up --build
```

## .gitignore

Este proyecto incluye un archivo `.gitignore` que asegura que no se suban archivos sensibles ni innecesarios al repositorio:

- **`venv/`**: El entorno virtual.
- **`.env`**: Archivo de configuración del entorno.
- **`__pycache__/`**: Archivos cacheados por Python.
- **Archivos de configuración de IDEs**: Para que las configuraciones locales no se incluyan en el repositorio.

Esto iniciará el servidor de FastAPI y la aplicación estará disponible en `http://127.0.0.1:8000/`.

## Pruebas

Para ejecutar las pruebas unitarias y de integración, puedes usar `pytest`:

```bash
pytest
```

## Contribución

1. Haz un fork del repositorio.
2. Crea una nueva rama con tus cambios (`git checkout -b feature/nueva-feature`).
3. Realiza un commit de tus cambios (`git commit -am 'Añadir nueva feature'`).
4. Haz push a la rama (`git push origin feature/nueva-feature`).
5. Abre un Pull Request.

## Licencia

Este proyecto está bajo la licencia [MIT](https://opensource.org/licenses/MIT).