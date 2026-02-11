# 🚀 NestJS GraphQL API – Docker + CI/CD + GitHub Actions

Backend API desarrollada con NestJS + GraphQL, dockerizada con multi-stage builds e integrada con GitHub Actions CI/CD para construir, versionar y publicar automáticamente imágenes Docker en Docker Hub.

Este proyecto simula un flujo DevOps profesional real, donde cada cambio en main genera automáticamente una nueva imagen lista para producción.

# ✅ Características

- Docker multi-stage builds
- Imagen ligera optimizada para producción
- GitHub Actions (CI/CD)
- Versionado semántico automático
- Publicación automática a Docker Hub



# 🧠 ¿Qué pasa cuando haces push?

Cada vez que ejecutas: `git push main`

```bush
Automáticamente:

GitHub Actions
   ↓
Calcula versión
   ↓
Docker build
   ↓
Tag version + latest
   ↓
Docker push (Docker Hub)
```

Resultado:
👉 nueva imagen disponible sin intervención manual

Eso es Continuous Integration + Continuous Delivery.


# 📁 Estructura del proyecto
```bush
.
├── .github/workflows/docker-image.yml
├── src/
├── test/
├── Dockerfile
├── package.json
├── yarn.lock
├── .dockerignore
```
# 🔄 CI/CD – GitHub Actions

Workflow:

`.github/workflows/docker-image.yml`


Se ejecuta en:

`push a main`

`pull request a main`

# 🔐 Secrets necesarios (GitHub)

Configurar en:

Settings → Secrets → Actions


Agregar:
```bush
DOCKER_USER
DOCKER_PASSWORD
```
