1. Objetivo del Documento
# Atlanticlifts - IMPLEMENTATION.md

## Objetivo

Este documento define las reglas técnicas para el desarrollo del sitio web de Atlanticlifts.

El objetivo es garantizar un código limpio, escalable y mantenible, siguiendo buenas prácticas de arquitectura Frontend, rendimiento, accesibilidad y SEO.

El desarrollador o IA deberá seguir estas directrices durante toda la implementación.

Siempre que exista conflicto entre PROJECT.md e IMPLEMENTATION.md, prevalecerá PROJECT.md respecto al diseño y experiencia de usuario, e IMPLEMENTATION.md respecto a la implementación técnica.
2. Stack Tecnológico
## Tecnologías

### Frontend

- React 19
- TypeScript
- Vite
- Tailwind CSS v4
- Framer Motion
- React Router DOM
- React Hook Form
- Zod
- TanStack Query
- Lucide React
- Swiper
- React Helmet Async

### Backend

- Node.js
- Express
- Multer
- Sharp
- Nodemailer
- JWT

### Base de Datos

- PostgreSQL

### Deploy

Frontend:
- Vercel

Backend:
- Render

Repositorio:
- GitHub

Nota: Aunque para la landing no se requiere una base de datos compleja, usar PostgreSQL deja el proyecto preparado para un futuro CMS, formularios avanzados o panel administrativo.

3. Reglas Generales
## Reglas de Desarrollo

- Utilizar TypeScript en todo el proyecto.
- No utilizar JavaScript.
- No utilizar CSS tradicional.
- Todo el estilo debe implementarse mediante Tailwind CSS.
- Evitar estilos inline.
- No duplicar componentes.
- Priorizar composición sobre herencia.
- Componentes pequeños y reutilizables.
- Una única responsabilidad por componente.
- Código legible antes que código complejo.
4. Arquitectura
src/

assets/
components/
sections/
layouts/
pages/
hooks/
services/
context/
types/
constants/
utils/
animations/
styles/
seo/

Cada carpeta tendrá una responsabilidad clara y no deberá mezclar lógica de negocio con presentación.

5. Convenciones
Componentes:
PascalCase

Hooks:
useNombreHook

Tipos:
Nombre.types.ts

Utilidades:
camelCase

Constantes:
UPPER_CASE

Archivos:
PascalCase para componentes.
camelCase para funciones.
6. Componentes

Cada componente deberá tener la siguiente estructura:

Button/

Button.tsx

Button.types.ts

Button.test.tsx

index.ts

Los componentes complejos podrán incluir carpetas adicionales para hooks, constantes o animaciones.

7. Gestión del Estado
Utilizar:

Estado Local
- useState
- useReducer

Estado Global
- Theme
- Drawer Mobile
- Preferencias del usuario

Datos remotos
- TanStack Query

No utilizar Redux.
8. Formularios
Todos los formularios deberán utilizar:

React Hook Form

+

Zod

Requisitos:

- Validación en tiempo real.
- Mensajes claros.
- Accesibilidad.
- Estados:
  - Loading
  - Error
  - Success
9. Animaciones
Todas las animaciones deberán implementarse con Framer Motion.

No utilizar librerías adicionales.

Principios:

- Animaciones discretas.
- 60 FPS.
- Compatibles con prefers-reduced-motion.
- Sin bloquear la interacción del usuario.
10. Imágenes y Videos
Imágenes

Formato preferido:

- AVIF
- WebP

Lazy Loading obligatorio.

Videos

Formato:

MP4
WebM

Todos los videos deberán incluir:

- poster
- muted
- loop
- autoplay
- playsInline

Optimizar peso antes del despliegue.
11. SEO
Cada página deberá incluir:

- Title
- Meta Description
- Open Graph
- Twitter Cards
- Canonical
- Robots
- Sitemap
- JSON-LD
12. Accesibilidad
Cumplir WCAG 2.2 AA.

Implementar:

- Navegación por teclado.
- Focus visible.
- Etiquetas ARIA.
- Contraste adecuado.
- Textos alternativos en imágenes.
- Respeto por prefers-reduced-motion.
13. Rendimiento
Objetivos Lighthouse

Performance ≥ 95

Accessibility ≥ 100

Best Practices ≥ 100

SEO ≥ 100

Core Web Vitals:

LCP < 2.5 s

CLS < 0.1

INP < 200 ms
14. Calidad del Código
Herramientas

- ESLint
- Prettier
- Husky
- lint-staged

Todo commit deberá pasar validaciones antes de integrarse.

Mantener consistencia en formato y estilo.
15. Seguridad
Nunca almacenar secretos en el frontend.

Variables sensibles mediante .env.

Validar entradas del usuario tanto en frontend como en backend.

Configurar cabeceras HTTP seguras.
16. Git
Convención de ramas

main

develop

feature/nombre-funcionalidad

fix/nombre-error

hotfix/nombre

Commits siguiendo Conventional Commits.

Ejemplos:

feat:

fix:

docs:

refactor:

style:

test:

chore:
17. Checklist antes del Deploy
Antes de publicar:

☐ Lighthouse ≥ objetivos.

☐ Sin errores de TypeScript.

☐ Sin advertencias de ESLint.

☐ Responsive validado.

☐ Dark Mode validado.

☐ Formularios funcionando.

☐ Videos optimizados.

☐ SEO completo.

☐ Accesibilidad validada.

☐ Todas las rutas funcionando.

☐ Assets comprimidos.

☐ Sin dependencias innecesarias.