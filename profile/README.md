# 🚀 Convenciones y nomenclaturas del proyecto

¡Bienvenido al proyecto! 👋

Para mantener nuestro código organizado, facilitar el trabajo en equipo y evitar confusiones, definimos las siguientes convenciones para los repositorios, las ramas de Git y el versionado del proyecto.

La idea es que todos trabajemos bajo los mismos estándares para que el desarrollo, el mantenimiento y los despliegues sean más sencillos.

## 📌 1. Información general

- **Nombre del proyecto:** `[NOMBRE_DEL_PROYECTO]`

## 📂 2. Nomenclatura de repositorios

Para identificar fácilmente cada parte de la aplicación, los repositorios seguirán el formato:

`<tecnología>-<nombre-del-proyecto>`

Utilizaremos **Kebab Case**: todo en minúsculas y con guiones medios (`-`) para separar las palabras.

| Componente | Formato | Ejemplo |
|---|---|---|
| Backend | `django-<nombre-del-proyecto>` | `django-gestion-academica` |
| Frontend | `react-<nombre-del-proyecto>` | `react-gestion-academica` |

**💡 ¿Por qué lo hacemos así?**

Porque podremos reconocer rápidamente la tecnología y el propósito de cada repositorio.

## 🌿 3. Nomenclatura de ramas (Branches)

Cada rama debe tener un nombre claro y descriptivo que permita identificar el tipo de trabajo que se está realizando.

Utilizaremos **Kebab Case** y la siguiente estructura:

`<tipo>/<id-issue>-<descripcion-corta>`

El ID del issue es opcional, pero recomendamos incluirlo para relacionar el código con la tarea correspondiente.

**Ejemplo:**

`feature/123-nueva-pasarela-pagos`

### 🛠️ Tipos de ramas

| Prefijo | ¿Cuándo utilizarlo? | Ejemplo |
|---|---|---|
| `feature/` | Para desarrollar nuevas funcionalidades. | `feature/123-login-usuarios` |
| `fix/` | Para corregir errores detectados durante el desarrollo o las pruebas. | `fix/124-error-validacion` |
| `hotfix/` | Para solucionar errores críticos en producción. | `hotfix/125-error-autenticacion` |
| `docs/` | Para crear o actualizar documentación. | `docs/126-actualizar-readme` |
| `chore/` | Para tareas de mantenimiento, configuración o actualización de dependencias. | `chore/127-actualizar-dependencias` |
| `test/` | Para agregar o corregir pruebas automatizadas. | `test/128-pruebas-usuarios` |

**✅ Buenas prácticas para crear ramas**

- Utiliza nombres cortos, claros y descriptivos.
- Escribe siempre en minúsculas.
- Separa las palabras con guiones medios (`-`).
- Evita espacios, tildes y caracteres especiales.
- Incluye el ID del issue cuando exista.
- Utiliza el prefijo que mejor represente el objetivo de tu tarea.

## 🏷️ 4. Versionado y etiquetas (Tags)

Para llevar un control claro de las versiones y sus cambios, utilizaremos **Semantic Versioning (SemVer)** o versionado semántico.

El formato será:

`vX.Y.Z`

Por ejemplo: `v1.2.3`

### 🔢 ¿Qué significa cada número?

El versionado sigue el formato `vX.Y.Z`, donde cada número representa un tipo de cambio:

| Número | Tipo | ¿Cuándo se incrementa? | Ejemplo |
|---|---|---|---|
| `X` | **Major (Mayor)** | Cuando se realizan cambios incompatibles con versiones anteriores. | `v1.5.0` → `v2.0.0` |
| `Y` | **Minor (Menor)** | Cuando se agregan nuevas funcionalidades compatibles con versiones anteriores. | `v1.2.3` → `v1.3.0` |
| `Z` | **Patch (Parche)** | Cuando se corrigen errores sin afectar la compatibilidad. | `v1.2.3` → `v1.2.4` |

**En resumen:**

- 🔴 **Major:** cambios importantes que pueden romper la compatibilidad.
- 🟡 **Minor:** nuevas funcionalidades que mantienen la compatibilidad.
- 🟢 **Patch:** correcciones de errores que no afectan la compatibilidad.

**Ejemplo práctico:** si tu proyecto está en la versión `v1.2.3` y corriges un error, la siguiente versión será `v1.2.4`. Si agregas una nueva funcionalidad compatible, será `v1.3.0`. Si introduces un cambio incompatible, será `v2.0.0`.

### 🚢 Creación de tags en Git

Cuando una versión estable esté lista y se despliegue a producción, crearemos un **tag** que identifique el commit exacto asociado a esa versión.

Esto nos permitirá consultar el código de cada lanzamiento y facilitará el seguimiento de las versiones desplegadas.

**Ejemplo: crear el primer release**

```bash
git tag -a v1.0.0 -m "Release inicial"
git push origin v1.0.0
```

El primer comando crea una etiqueta anotada y el segundo la publica en el repositorio remoto.

Para consultar las etiquetas existentes:

```bash
git tag
```

Para crear una nueva versión, recuerda elegir el incremento adecuado según el tipo de cambios realizados.

---

## 🤝 5. Nuestro compromiso

Estas convenciones buscan que el equipo trabaje de forma consistente, que el historial de cambios sea fácil de entender y que cada versión del proyecto pueda identificarse sin complicaciones.

**Antes de crear una rama o publicar una versión, revisa estas reglas y asegúrate de aplicarlas.**

¡Un código organizado facilita el trabajo de todos! 💻✨
