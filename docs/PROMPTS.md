# Atlanticlifts Website - AI Prompt Library

> This document contains standardized prompts for AI-assisted development.
>
> Every prompt assumes the project documentation is available inside the `/docs` directory.
>
> Always start a new AI session with one of these prompts instead of writing instructions from scratch.

---

# Prompt 01 — Project Initialization

## Purpose

Initialize a new AI session with complete project context.

```
Read the following documents before doing anything:

docs/CONTEXT.md
docs/TASKS.md
docs/DECISIONS.md

These documents are the single source of truth for this project.

Do not generate code.

Analyze the project architecture, summarize your understanding, identify inconsistencies or improvement opportunities, and wait for my approval before implementing anything.
```

---

# Prompt 02 — Start Development

## Purpose

Begin implementing the next pending task.

```
Read:

docs/CONTEXT.md
docs/TASKS.md
docs/DECISIONS.md

Identify the first pending task.

Implement it completely.

Requirements:

- Follow the Design System.
- Follow the folder architecture.
- Use TypeScript.
- Use reusable components.
- Keep code clean and documented only when necessary.

When finished:

- Verify the build.
- Verify lint.
- Update TASKS.md.
```

---

# Prompt 03 — Continue Development

## Purpose

Resume an interrupted session.

```
Read:

docs/CONTEXT.md
docs/TASKS.md
docs/DECISIONS.md

Identify the last completed task.

Continue with the next pending task.

Do not modify completed tasks unless required.
```

---

# Prompt 04 — Code Review

## Purpose

Review recently implemented code.

```
Review the entire project.

Focus on:

Architecture
Code quality
TypeScript
Accessibility
Performance
Maintainability
Best practices

Do not rewrite code unless necessary.

Provide prioritized recommendations.
```

---

# Prompt 05 — Refactoring

## Purpose

Improve existing code.

```
Analyze the current implementation.

Refactor only where meaningful improvements exist.

Maintain all existing functionality.

Reduce duplication.

Improve readability.

Improve component composition.

Do not introduce breaking changes.
```

---

# Prompt 06 — UI Review

## Purpose

Evaluate the user interface.

```
Review the complete UI.

Evaluate:

Visual hierarchy
Spacing
Typography
Consistency
Responsiveness
Dark Mode
Accessibility
Animations

Provide recommendations to achieve a premium corporate design.
```

---

# Prompt 07 — Accessibility Audit

## Purpose

Accessibility review.

```
Perform a complete accessibility audit.

Check:

Semantic HTML

ARIA

Keyboard Navigation

Focus States

Contrast

Reduced Motion

Screen Reader Compatibility

Target:

WCAG AA
```

---

# Prompt 08 — Performance Audit

## Purpose

Optimize the application.

```
Review the project for performance.

Focus on:

Bundle size

Code splitting

Image optimization

Video optimization

Caching

Rendering strategy

Lazy loading

Target:

Lighthouse >95
```

---

# Prompt 09 — SEO Audit

## Purpose

SEO optimization.

```
Review every page.

Check:

Metadata

Open Graph

Twitter Cards

JSON-LD

Canonical URLs

Heading hierarchy

Semantic HTML

Internal linking

Sitemap

Robots.txt

Generate recommendations.
```

---

# Prompt 10 — Component Generation

## Purpose

Create a reusable component.

```
Generate a production-ready React component.

Requirements:

TypeScript

Tailwind CSS

Reusable

Accessible

Responsive

Dark Mode compatible

Well structured

Follow the Design System

Avoid hardcoded values.
```

---

# Prompt 11 — Animation Generation

## Purpose

Create premium animations.

```
Generate smooth animations using Framer Motion.

Requirements:

Subtle

Elegant

Premium

Accessible

Respect reduced-motion preferences.

Avoid excessive motion.

Optimize performance.
```

---

# Prompt 12 — Documentation Update

## Purpose

Keep documentation synchronized.

```
Review the project.

Identify any changes that require documentation updates.

Update:

TASKS.md

DECISIONS.md

CHANGELOG.md

Do not modify CONTEXT.md unless project fundamentals have changed.
```

---

# Prompt 13 — Final Production Review

## Purpose

Prepare for deployment.

```
Perform a complete production review.

Verify:

Architecture

TypeScript

Build

Lint

Accessibility

SEO

Performance

Security

Responsive Design

Dark Mode

Documentation

Generate a deployment checklist.

Only approve deployment if all requirements are satisfied.
```

---

# AI Workflow

Every AI session must follow this workflow:

1. Read CONTEXT.md
2. Read TASKS.md
3. Read DECISIONS.md
4. Analyze current state
5. Implement only the requested task
6. Validate changes
7. Update documentation
8. Wait for the next instruction

Never skip steps.

---

# General Rules

* Never ignore project documentation.
* Never install dependencies without justification.
* Never duplicate code.
* Prefer reusable components.
* Follow the Design System.
* Use strict TypeScript.
* Keep accessibility as a priority.
* Optimize before completing any task.
* Document important architectural changes.
