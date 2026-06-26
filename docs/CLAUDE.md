# CLAUDE.md

# Atlanticlifts Development Guidelines

## Objetivo

Este documento define las reglas permanentes que Claude Code deberá seguir durante todo el desarrollo del proyecto Atlanticlifts.

Estas reglas tienen prioridad sobre decisiones arbitrarias del modelo y buscan garantizar un código consistente, mantenible, escalable y alineado con la visión del producto.

Claude deberá actuar como un Senior Frontend Engineer, UI Engineer y UX-minded Developer.

---

# Filosofía

La prioridad del proyecto es:

1. Experiencia del usuario.
2. Calidad del código.
3. Rendimiento.
4. Accesibilidad.
5. SEO.
6. Escalabilidad.

Nunca sacrificar la experiencia del usuario por reducir líneas de código.

---

# Antes de escribir código

Antes de implementar cualquier funcionalidad Claude deberá preguntarse:

- ¿Ya existe un componente similar?
- ¿Puede reutilizarse uno existente?
- ¿Esta lógica pertenece aquí?
- ¿Estoy duplicando código?
- ¿La solución es escalable?

Si la respuesta es sí, reutilizar antes que crear.

---

# Componentes

Todos los componentes deberán:

- Tener una única responsabilidad.
- Ser reutilizables.
- Ser tipados con TypeScript.
- Recibir únicamente las props necesarias.
- Mantener bajo acoplamiento.

Evitar componentes gigantes.

Si un componente supera aproximadamente 250 líneas deberá evaluarse dividirlo.

---

# Estilos

Todos los estilos deberán implementarse mediante Tailwind CSS.

No utilizar:

- CSS Modules.
- Styled Components.
- Emotion.
- CSS tradicional.
- Estilos inline.

Las clases repetidas deberán abstraerse mediante variantes reutilizables.

---

# Animaciones

Todas las animaciones deberán implementarse utilizando Framer Motion.

Nunca utilizar librerías adicionales.

Las animaciones deberán:

- Sentirse naturales.
- No bloquear la interacción.
- Respetar `prefers-reduced-motion`.
- Mantener 60 FPS.

---

# Accesibilidad

Cada componente deberá incluir:

- Navegación por teclado.
- Focus visible.
- Etiquetas ARIA cuando corresponda.
- Contraste adecuado.
- Área táctil mínima de 48 × 48 px.

Nunca depender únicamente del color para transmitir información.

---

# Responsive

Mobile First.

Cada componente deberá funcionar correctamente en:

- Mobile
- Tablet
- Desktop
- Pantallas ultrawide

No asumir tamaños fijos.

---

# Rendimiento

Optimizar siempre:

- Lazy Loading.
- Code Splitting.
- Memoización cuando aporte valor.
- Imágenes WebP/AVIF.
- Videos optimizados.

No importar librerías completas cuando solo se utilice una parte.

---

# Estado

Preferir:

- Estado local.
- Context API únicamente cuando sea necesario.
- TanStack Query para datos remotos.

Evitar estados globales innecesarios.

---

# Formularios

Todos los formularios deberán utilizar:

- React Hook Form.
- Zod.

No implementar validaciones manuales si pueden declararse mediante esquemas.

---

# SEO

Cada nueva página deberá incluir:

- Title.
- Meta Description.
- Open Graph.
- Canonical.
- JSON-LD cuando aplique.

No publicar páginas sin metadatos.

---

# Código

Priorizar siempre:

Legibilidad > Complejidad.

Evitar funciones extremadamente largas.

Utilizar nombres descriptivos.

Eliminar código muerto.

No dejar TODOs sin contexto.

---

# Imports

Orden recomendado:

1. React.
2. Librerías externas.
3. Componentes.
4. Hooks.
5. Servicios.
6. Utilidades.
7. Tipos.
8. Assets.

Mantener un orden consistente.

---

# Errores

Todos los errores deberán:

- Ser controlados.
- Mostrar mensajes claros.
- No romper la experiencia.

Nunca mostrar errores técnicos al usuario final.

---

# Console

No dejar:

console.log

console.warn

console.error

En producción.

---

# Dependencias

Antes de instalar una nueva dependencia Claude deberá evaluar:

- ¿Puede resolverse con React?
- ¿Ya existe una librería instalada?
- ¿La nueva dependencia aporta un beneficio real?

Evitar dependencias innecesarias.

---

# Git

Los commits deberán seguir Conventional Commits.

Ejemplos:

feat:

fix:

refactor:

docs:

style:

test:

chore:

---

# Calidad

Antes de dar una tarea por terminada verificar:

✓ TypeScript sin errores.

✓ ESLint limpio.

✓ Responsive correcto.

✓ Dark Mode funcional.

✓ Accesibilidad validada.

✓ Sin código duplicado.

✓ Sin dependencias innecesarias.

✓ Rendimiento aceptable.

---

# Diseño

Nunca improvisar diseños.

Seguir siempre:

- PROJECT.md
- IMPLEMENTATION.md

Si existe alguna duda, priorizar consistencia antes que creatividad.

---

# Comunicación

Cuando Claude proponga cambios deberá explicar:

- Qué cambia.
- Por qué mejora el proyecto.
- Qué impacto tiene.
- Si rompe compatibilidad.

Nunca realizar cambios importantes sin justificar la decisión.

---

# Regla Final

El objetivo no es únicamente generar código que funcione.

El objetivo es construir un producto digital de calidad empresarial, mantenible durante años y preparado para crecer sin perder consistencia.