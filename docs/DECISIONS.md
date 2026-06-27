# Atlanticlifts Website - Architecture Decision Records (ADR)

> This document records all important technical and architectural decisions made throughout the project.
>
> Every AI assistant and developer must read this document before proposing architectural changes.
>
> Decisions should not be changed without a documented reason.

---

# ADR-001

## Title

Use Next.js instead of React + Vite

### Status

Accepted

### Date

2026-06-26

### Context

The website is intended to be the primary digital presence of Atlanticlifts, with a strong focus on SEO, performance, scalability and future growth.

### Alternatives Considered

* React + Vite
* Next.js

### Decision

The project will use Next.js with the App Router.

### Reasons

* Better SEO
* Server Side Rendering
* Static Site Generation
* Image optimization
* Font optimization
* Excellent Vercel integration
* Better long-term scalability

### Consequences

Positive

* Higher search engine visibility.
* Better performance.
* Easier deployment.

Negative

* Slightly steeper learning curve.

---

# ADR-002

## Title

Deploy on Vercel

### Status

Accepted

### Context

The project requires automatic deployments, previews and global CDN.

### Alternatives

* Vercel
* Netlify
* AWS
* Azure

### Decision

Deploy using Vercel.

### Reasons

* Native Next.js support
* Preview Deployments
* Automatic HTTPS
* CDN
* Edge Network

---

# ADR-003

## Title

Use Tailwind CSS

### Status

Accepted

### Decision

Tailwind CSS is the official styling solution.

### Reasons

* Utility-first
* Excellent developer experience
* Small production bundle
* Easy Design System implementation

---

# ADR-004

## Title

Use shadcn/ui only for reusable UI primitives

### Status

Accepted

### Context

Atlanticlifts requires a unique visual identity.

### Decision

Only low-level UI components will use shadcn/ui.

Examples

* Button
* Input
* Dialog
* Sheet
* Tooltip
* Accordion
* Form
* Select

High-level sections must be custom-built.

Examples

* Hero
* Navbar
* Services
* Industries
* Projects
* Footer
* CTA

### Reasons

* Maintain brand identity.
* Avoid generic layouts.
* Easier customization.

---

# ADR-005

## Title

Use Framer Motion

### Status

Accepted

### Alternatives

* GSAP
* Motion One
* CSS Animations

### Decision

Use Framer Motion.

### Reasons

* React-first
* Declarative API
* Excellent performance
* Great developer experience

---

# ADR-006

## Title

Design System First

### Status

Accepted

### Decision

No page implementation starts before the Design System is complete.

### Reasons

* Consistency
* Maintainability
* Scalability

---

# ADR-007

## Title

Feature-Based Architecture

### Status

Accepted

### Decision

Business logic should be organized by features.

### Reasons

* Better scalability
* Better separation of concerns
* Easier maintenance

---

# ADR-008

## Title

Dark Mode is mandatory

### Status

Accepted

### Decision

Every component must support both Light and Dark themes.

### Reasons

* Better user experience
* Modern web standards
* Improved accessibility

---

# ADR-009

## Title

Documentation First Development

### Status

Accepted

### Decision

Every significant implementation must be documented before development begins.

### Required Documents

* CONTEXT.md
* TASKS.md
* ROADMAP.md
* IMPLEMENTATION.md
* DECISIONS.md

---

# ADR-010

## Title

AI-Assisted Development Workflow

### Status

Accepted

### Decision

The project follows a structured AI workflow.

Workflow

1. Read CONTEXT.md
2. Read TASKS.md
3. Read DECISIONS.md
4. Analyze requirements
5. Implement code
6. Validate
7. Update TASKS.md

---

# Future Decisions

Reserve this section for future architectural decisions such as:

* CMS integration
* Internationalization (i18n)
* Blog implementation
* Analytics provider
* Authentication
* Contact API
* Dashboard
* Headless CMS
* Database selection

---

# Decision Rules

Every new architectural decision must include:

* Title
* Date
* Status
* Context
* Alternatives
* Final Decision
* Justification
* Consequences

No architectural decision should be modified without documenting the reason.
