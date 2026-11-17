# Guía de contribución

Gracias por querer colaborar en **TechECS**. Estas normas valen para todos los repositorios de la organización salvo que uno tenga su propia guía.

## Flujo de trabajo

1. Crea una **rama** a partir de `main`. No hagas commits directamente en `main`.
2. Haz tus cambios y abre un **Pull Request**.
3. Espera a que pasen las comprobaciones automáticas y a la revisión.
4. El PR se integra con **squash merge**: `main` recibe un único commit por PR.

## Conventional Commits

Los commits y, sobre todo, el **título del PR** siguen [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/):

```
tipo(ámbito opcional): descripción
```

- En minúsculas, en imperativo, sin punto final y de **72 caracteres como máximo**.
- Si hay un cambio incompatible, añade `!` tras el tipo (`feat(api)!: ...`) y explica `BREAKING CHANGE:` en el pie.
- En el cuerpo, explica el **qué** y el **porqué**, separado de la cabecera por una línea en blanco.

**Tipos permitidos:** `feat`, `fix`, `refactor`, `style`, `perf`, `docs`, `chore`, `build`, `ci`, `test`.

Ejemplos:

```
feat(login): añade acceso con enlace mágico
fix: corrige el redirect tras cerrar sesión
refactor(core)!: elimina la api de sesiones antigua
```

## Comprobaciones automáticas

Los workflows compartidos viven en [`org-ci-workflows`](https://github.com/TechECS/org-ci-workflows). Algunos repositorios validan el título del PR y otros pueden normalizar automáticamente el mensaje del último commit. En ese caso, si tu rama local queda divergente de la remota, ejecuta `git pull --rebase`.

## Seguridad

Si encuentras una vulnerabilidad, **no abras un issue**: sigue la [política de seguridad](SECURITY.md).
