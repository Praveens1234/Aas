# 🤖 AI Agent Skill Document: Full-Stack Development (Frontend & Backend)

> **Version:** 2.0.0
> **Last Updated:** 2025-07-11
> **Classification:** Production-Ready Skill Set
> **Proficiency Target:** Expert-Level Full-Stack Engineering

---

## 📑 Table of Contents

1. [Skill Overview & Philosophy](#1-skill-overview--philosophy)
2. [Frontend Development](#2-frontend-development)
   - 2.1 [Core Web Technologies](#21-core-web-technologies)
   - 2.2 [Frontend Frameworks & Libraries](#22-frontend-frameworks--libraries)
   - 2.3 [State Management](#23-state-management)
   - 2.4 [Styling & UI Systems](#24-styling--ui-systems)
   - 2.5 [Performance Optimization](#25-performance-optimization)
   - 2.6 [Accessibility (a11y)](#26-accessibility-a11y)
   - 2.7 [Testing (Frontend)](#27-testing-frontend)
3. [Backend Development](#3-backend-development)
   - 3.1 [Server-Side Languages & Runtimes](#31-server-side-languages--runtimes)
   - 3.2 [Backend Frameworks](#32-backend-frameworks)
   - 3.3 [API Design & Architecture](#33-api-design--architecture)
   - 3.4 [Database Design & Management](#34-database-design--management)
   - 3.5 [Authentication & Authorization](#35-authentication--authorization)
   - 3.6 [Caching Strategies](#36-caching-strategies)
   - 3.7 [Testing (Backend)](#37-testing-backend)
4. [Architecture & Design Patterns](#4-architecture--design-patterns)
5. [DevOps, CI/CD & Deployment](#5-devops-cicd--deployment)
6. [Security Best Practices](#6-security-best-practices)
7. [Code Quality Standards](#7-code-quality-standards)
8. [Agent Behavior Rules & Decision Framework](#8-agent-behavior-rules--decision-framework)
9. [Project Scaffolding Templates](#9-project-scaffolding-templates)
10. [Troubleshooting Playbook](#10-troubleshooting-playbook)
11. [Technology Decision Matrix](#11-technology-decision-matrix)
12. [Glossary](#12-glossary)

---

## 1. Skill Overview & Philosophy

### 1.1 Purpose

This document defines the **complete skill set, behavioral rules, decision-making frameworks, and best practices** an AI agent must follow when performing frontend and backend development tasks. It serves as the **single source of truth** for code generation, architecture decisions, debugging, and engineering guidance.

### 1.2 Core Engineering Principles

```
┌──────────────────────────────────────────────────────────────────┐
│                    ENGINEERING PRINCIPLES                        │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. CORRECTNESS    → Code must work as intended, always.        │
│  2. CLARITY        → Code is read 10x more than written.        │
│  3. SIMPLICITY     → Prefer simple over clever.                 │
│  4. SECURITY       → Never trust user input. Ever.              │
│  5. PERFORMANCE    → Measure first, optimize second.            │
│  6. SCALABILITY    → Design for 10x, build for 1x.             │
│  7. TESTABILITY    → If it's not tested, it's broken.           │
│  8. MAINTAINABILITY→ Future-you is a different person.          │
│  9. ACCESSIBILITY  → Build for everyone, not just some.         │
│ 10. DOCUMENTATION  → Code without docs is legacy code.          │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 1.3 Agent Operational Rules

| Rule | Description |
|------|-------------|
| **R-001** | Always ask clarifying questions before building complex systems |
| **R-002** | Default to TypeScript over JavaScript unless explicitly requested |
| **R-003** | Always include error handling — never leave promises uncaught |
| **R-004** | Generate production-ready code, not prototypes (unless asked) |
| **R-005** | Include inline comments for complex logic, not obvious code |
| **R-006** | Follow the project's existing code style if provided |
| **R-007** | Suggest tests alongside feature code |
| **R-008** | Flag security vulnerabilities proactively |
| **R-009** | Provide multiple options when trade-offs exist |
| **R-010** | Always specify package versions in dependency recommendations |

---

## 2. Frontend Development

### 2.1 Core Web Technologies

#### 2.1.1 HTML5 — Semantic Markup

**Skill Level:** Expert

```html
<!-- ❌ BAD: Non-semantic, div soup -->
<div class="header">
  <div class="nav">
    <div class="nav-item">Home</div>
  </div>
</div>
<div class="main">
  <div class="article">
    <div class="title">Article Title</div>
    <div class="content">Content here...</div>
  </div>
</div>

<!-- ✅ GOOD: Semantic, accessible, SEO-friendly -->
<header role="banner">
  <nav aria-label="Primary navigation">
    <ul>
      <li><a href="/" aria-current="page">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </nav>
</header>
<main role="main">
  <article>
    <header>
      <h1>Article Title</h1>
      <time datetime="2025-07-11">July 11, 2025</time>
    </header>
    <section aria-labelledby="intro-heading">
      <h2 id="intro-heading">Introduction</h2>
      <p>Content here...</p>
    </section>
    <footer>
      <p>Written by <address><a href="mailto:author@example.com">Author</a></address></p>
    </footer>
  </article>
</main>
<footer role="contentinfo">
  <p>&copy; 2025 Company Name</p>
</footer>
```

**Key HTML5 Elements & When to Use Them:**

| Element | Purpose | Use Case |
|---------|---------|----------|
| `<header>` | Introductory content | Page header, article header |
| `<nav>` | Navigation links | Primary/secondary menus |
| `<main>` | Dominant content | One per page |
| `<article>` | Self-contained content | Blog posts, news articles |
| `<section>` | Thematic grouping | Chapters, tab panels |
| `<aside>` | Tangentially related | Sidebars, callouts |
| `<figure>` | Self-contained media | Images with captions |
| `<details>` | Expandable widget | FAQs, collapsibles |
| `<dialog>` | Modal/non-modal dialog | Confirmations, forms |
| `<template>` | Inert HTML fragment | Client-side rendering |

#### 2.1.2 CSS3 — Modern Styling

**Skill Level:** Expert

```css
/* ============================================
   MODERN CSS ARCHITECTURE
   Methodology: Custom Properties + Utility Layer
   ============================================ */

/* --- DESIGN TOKENS (Custom Properties) --- */
:root {
  /* Color System */
  --color-primary-50: #eff6ff;
  --color-primary-100: #dbeafe;
  --color-primary-500: #3b82f6;
  --color-primary-600: #2563eb;
  --color-primary-700: #1d4ed8;
  --color-primary-900: #1e3a5f;

  --color-neutral-0: #ffffff;
  --color-neutral-50: #f9fafb;
  --color-neutral-100: #f3f4f6;
  --color-neutral-500: #6b7280;
  --color-neutral-900: #111827;

  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;

  /* Typography Scale (Major Third - 1.25) */
  --font-family-sans: 'Inter', system-ui, -apple-system, sans-serif;
  --font-family-mono: 'JetBrains Mono', 'Fira Code', monospace;

  --font-size-xs: clamp(0.7rem, 0.66rem + 0.2vw, 0.8rem);
  --font-size-sm: clamp(0.8rem, 0.76rem + 0.22vw, 0.9rem);
  --font-size-base: clamp(1rem, 0.95rem + 0.25vw, 1.125rem);
  --font-size-lg: clamp(1.25rem, 1.18rem + 0.33vw, 1.41rem);
  --font-size-xl: clamp(1.56rem, 1.48rem + 0.42vw, 1.76rem);
  --font-size-2xl: clamp(1.95rem, 1.85rem + 0.52vw, 2.2rem);
  --font-size-3xl: clamp(2.44rem, 2.31rem + 0.65vw, 2.75rem);

  /* Spacing Scale (8px base) */
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-24: 6rem;     /* 96px */

  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);

  /* Border Radius */
  --radius-sm: 0.25rem;
  --radius-md: 0.5rem;
  --radius-lg: 1rem;
  --radius-full: 9999px;

  /* Transitions */
  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);

  /* Z-Index Scale */
  --z-dropdown: 100;
  --z-sticky: 200;
  --z-overlay: 300;
  --z-modal: 400;
  --z-toast: 500;
  --z-tooltip: 600;
}

/* --- DARK MODE --- */
@media (prefers-color-scheme: dark) {
  :root {
    --color-neutral-0: #111827;
    --color-neutral-50: #1f2937;
    --color-neutral-100: #374151;
    --color-neutral-500: #9ca3af;
    --color-neutral-900: #f9fafb;
  }
}

/* --- MODERN LAYOUT PATTERNS --- */

/* Container Query (Modern Responsive Design) */
.card-container {
  container-type: inline-size;
  container-name: card;
}

@container card (min-width: 400px) {
  .card {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: var(--space-4);
  }
}

/* CSS Grid — Auto-fit Responsive Grid */
.auto-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
  gap: var(--space-6);
}

/* Flexbox — Centered Layout */
.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100svh; /* Uses small viewport height */
}

/* Modern Scroll Snap */
.carousel {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;
  scrollbar-width: thin;
}

.carousel > * {
  scroll-snap-align: start;
  flex-shrink: 0;
}

/* --- ANIMATION --- */
@keyframes fade-in {
  from { opacity: 0; translate: 0 1rem; }
  to { opacity: 1; translate: 0 0; }
}

.animate-in {
  animation: fade-in var(--transition-base) both;
}

/* Respect reduced motion */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

#### 2.1.3 JavaScript / TypeScript — Modern Patterns

**Skill Level:** Expert

```typescript
// ============================================
// TYPESCRIPT BEST PRACTICES & PATTERNS
// ============================================

// --- STRICT TYPE DEFINITIONS ---
// Always prefer interfaces for objects, types for unions/intersections

interface User {
  readonly id: string;
  email: string;
  name: string;
  role: UserRole;
  preferences: UserPreferences;
  createdAt: Date;
  updatedAt: Date;
}

type UserRole = 'admin' | 'editor' | 'viewer';

interface UserPreferences {
  theme: 'light' | 'dark' | 'system';
  language: string;
  notifications: NotificationSettings;
}

interface NotificationSettings {
  email: boolean;
  push: boolean;
  frequency: 'instant' | 'daily' | 'weekly';
}

// --- UTILITY TYPES (Custom) ---
type Nullable<T> = T | null;
type Optional<T> = T | undefined;
type AsyncResult<T, E = Error> = Promise<Result<T, E>>;

// Result type for explicit error handling (no throwing)
type Result<T, E = Error> =
  | { success: true; data: T }
  | { success: false; error: E };

// Deep Partial for patch operations
type DeepPartial<T> = {
  [P in keyof T]?: T[P] extends object ? DeepPartial<T[P]> : T[P];
};

// --- FUNCTIONAL ERROR HANDLING ---
function createResult<T>(data: T): Result<T> {
  return { success: true, data };
}

function createError<E = Error>(error: E): Result<never, E> {
  return { success: false, error };
}

async function trySafe<T>(
  fn: () => Promise<T>
): AsyncResult<T> {
  try {
    const data = await fn();
    return createResult(data);
  } catch (error) {
    return createError(
      error instanceof Error ? error : new Error(String(error))
    );
  }
}

// Usage:
async function fetchUser(id: string): AsyncResult<User> {
  return trySafe(async () => {
    const response = await fetch(`/api/users/${id}`);
    if (!response.ok) {
      throw new Error(`HTTP ${response.status}: ${response.statusText}`);
    }
    return response.json();
  });
}

// Consuming result:
async function displayUser(id: string): Promise<void> {
  const result = await fetchUser(id);

  if (!result.success) {
    console.error('Failed to fetch user:', result.error.message);
    return;
  }

  console.log('User:', result.data.name);
}

// --- MODERN JAVASCRIPT PATTERNS ---

// 1. Structured Clone (Deep Copy)
const original = { nested: { value: 42 } };
const cloned = structuredClone(original);

// 2. Object.groupBy (ES2024)
const users: User[] = [/* ... */];
const grouped = Object.groupBy(users, (user) => user.role);

// 3. Promise.withResolvers (ES2024)
function createDeferredPromise<T>() {
  const { promise, resolve, reject } = Promise.withResolvers<T>();
  return { promise, resolve, reject };
}

// 4. Using declarations (explicit resource management)
// Symbol.dispose for sync, Symbol.asyncDispose for async
class DatabaseConnection {
  [Symbol.asyncDispose]() {
    return this.close();
  }
  async close() { /* cleanup */ }
  async query(sql: string) { /* ... */ }
}

// 5. Immutable update patterns
function updateUser(user: User, updates: DeepPartial<User>): User {
  return {
    ...user,
    ...updates,
    preferences: {
      ...user.preferences,
      ...(updates.preferences ?? {}),
      notifications: {
        ...user.preferences.notifications,
        ...(updates.preferences?.notifications ?? {}),
      },
    },
    updatedAt: new Date(),
  };
}

// 6. Builder Pattern for complex objects
class QueryBuilder<T> {
  private filters: Array<(item: T) => boolean> = [];
  private sortFn?: (a: T, b: T) => number;
  private limitCount?: number;
  private offsetCount = 0;

  where(predicate: (item: T) => boolean): this {
    this.filters.push(predicate);
    return this;
  }

  orderBy(compareFn: (a: T, b: T) => number): this {
    this.sortFn = compareFn;
    return this;
  }

  limit(count: number): this {
    this.limitCount = count;
    return this;
  }

  offset(count: number): this {
    this.offsetCount = count;
    return this;
  }

  execute(data: T[]): T[] {
    let result = data.filter((item) =>
      this.filters.every((filter) => filter(item))
    );

    if (this.sortFn) {
      result = result.sort(this.sortFn);
    }

    result = result.slice(this.offsetCount);

    if (this.limitCount !== undefined) {
      result = result.slice(0, this.limitCount);
    }

    return result;
  }
}
```

---

### 2.2 Frontend Frameworks & Libraries

#### 2.2.1 React (Primary Framework)

**Skill Level:** Expert | **Version:** 19.x

```
React Ecosystem Mastery Map
━━━━━━━━━━━━━━━━━━━━━━━━━━━
├── Core React
│   ├── Functional Components (exclusively)
│   ├── Hooks (built-in + custom)
│   ├── Server Components (RSC)
│   ├── Suspense & Error Boundaries
│   ├── Context API
│   ├── Refs & Forwarding Refs
│   ├── Portals
│   └── Strict Mode
├── Meta-Frameworks
│   ├── Next.js (App Router — primary)
│   ├── Remix
│   └── Astro (content-heavy)
├── State Management
│   ├── Zustand (recommended default)
│   ├── Jotai (atomic state)
│   ├── TanStack Query (server state)
│   └── Redux Toolkit (large teams)
├── Styling
│   ├── Tailwind CSS (recommended)
│   ├── CSS Modules
│   └── Styled Components
├── Forms
│   ├── React Hook Form + Zod
│   └── Formik + Yup (legacy)
├── Routing
│   ├── Next.js App Router
│   ├── TanStack Router
│   └── React Router v7
└── Data Fetching
    ├── TanStack Query
    ├── SWR
    └── Server Actions (Next.js)
```

**React Component Best Practices:**

```tsx
// ============================================
// PRODUCTION-GRADE REACT COMPONENT
// ============================================

import {
  forwardRef,
  memo,
  useCallback,
  useId,
  useMemo,
  useState,
  type ComponentPropsWithoutRef,
  type ReactNode,
} from 'react';
import { cva, type VariantProps } from 'class-variance-authority';
import { cn } from '@/lib/utils';

// --- VARIANT DEFINITION (using CVA) ---
const buttonVariants = cva(
  // Base styles
  [
    'inline-flex items-center justify-center gap-2',
    'rounded-md font-medium whitespace-nowrap',
    'transition-colors duration-200',
    'focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-offset-2',
    'disabled:pointer-events-none disabled:opacity-50',
    'select-none',
  ],
  {
    variants: {
      variant: {
        primary: [
          'bg-primary-600 text-white',
          'hover:bg-primary-700',
          'focus-visible:ring-primary-500',
          'active:bg-primary-800',
        ],
        secondary: [
          'bg-neutral-100 text-neutral-900',
          'hover:bg-neutral-200',
          'focus-visible:ring-neutral-500',
          'border border-neutral-300',
        ],
        destructive: [
          'bg-red-600 text-white',
          'hover:bg-red-700',
          'focus-visible:ring-red-500',
        ],
        ghost: [
          'text-neutral-700',
          'hover:bg-neutral-100',
          'focus-visible:ring-neutral-500',
        ],
        link: [
          'text-primary-600 underline-offset-4',
          'hover:underline',
        ],
      },
      size: {
        sm: 'h-8 px-3 text-sm',
        md: 'h-10 px-4 text-sm',
        lg: 'h-12 px-6 text-base',
        icon: 'h-10 w-10',
      },
    },
    defaultVariants: {
      variant: 'primary',
      size: 'md',
    },
  }
);

// --- TYPE DEFINITION ---
interface ButtonProps
  extends ComponentPropsWithoutRef<'button'>,
    VariantProps<typeof buttonVariants> {
  /** Show loading spinner and disable interactions */
  isLoading?: boolean;
  /** Icon to display before the label */
  leftIcon?: ReactNode;
  /** Icon to display after the label */
  rightIcon?: ReactNode;
}

// --- COMPONENT ---
const Button = forwardRef<HTMLButtonElement, ButtonProps>(
  (
    {
      className,
      variant,
      size,
      isLoading = false,
      leftIcon,
      rightIcon,
      disabled,
      children,
      ...props
    },
    ref
  ) => {
    return (
      <button
        ref={ref}
        className={cn(buttonVariants({ variant, size }), className)}
        disabled={disabled || isLoading}
        aria-busy={isLoading}
        {...props}
      >
        {isLoading ? (
          <Spinner className="h-4 w-4 animate-spin" aria-hidden="true" />
        ) : (
          leftIcon
        )}
        {children}
        {rightIcon && !isLoading && rightIcon}
      </button>
    );
  }
);

Button.displayName = 'Button';

export { Button, buttonVariants };
export type { ButtonProps };

// --- SPINNER COMPONENT ---
function Spinner({ className, ...props }: ComponentPropsWithoutRef<'svg'>) {
  return (
    <svg
      className={cn('animate-spin', className)}
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      {...props}
    >
      <circle
        className="opacity-25"
        cx="12"
        cy="12"
        r="10"
        stroke="currentColor"
        strokeWidth="4"
      />
      <path
        className="opacity-75"
        fill="currentColor"
        d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z"
      />
    </svg>
  );
}


// ============================================
// CUSTOM HOOKS — PRODUCTION PATTERNS
// ============================================

// --- useDebounce ---
import { useEffect, useState } from 'react';

function useDebounce<T>(value: T, delay: number): T {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timer = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(timer);
  }, [value, delay]);

  return debouncedValue;
}

// --- useLocalStorage ---
function useLocalStorage<T>(
  key: string,
  initialValue: T
): [T, (value: T | ((prev: T) => T)) => void] {
  const [storedValue, setStoredValue] = useState<T>(() => {
    if (typeof window === 'undefined') return initialValue;
    try {
      const item = window.localStorage.getItem(key);
      return item ? (JSON.parse(item) as T) : initialValue;
    } catch (error) {
      console.warn(`Error reading localStorage key "${key}":`, error);
      return initialValue;
    }
  });

  const setValue = useCallback(
    (value: T | ((prev: T) => T)) => {
      setStoredValue((prev) => {
        const nextValue = value instanceof Function ? value(prev) : value;
        try {
          window.localStorage.setItem(key, JSON.stringify(nextValue));
        } catch (error) {
          console.warn(`Error setting localStorage key "${key}":`, error);
        }
        return nextValue;
      });
    },
    [key]
  );

  return [storedValue, setValue];
}

// --- useMediaQuery ---
function useMediaQuery(query: string): boolean {
  const [matches, setMatches] = useState(() => {
    if (typeof window === 'undefined') return false;
    return window.matchMedia(query).matches;
  });

  useEffect(() => {
    const mql = window.matchMedia(query);
    const handler = (e: MediaQueryListEvent) => setMatches(e.matches);

    mql.addEventListener('change', handler);
    return () => mql.removeEventListener('change', handler);
  }, [query]);

  return matches;
}

// --- useFetch (with TanStack Query pattern) ---
interface UseFetchOptions<T> {
  enabled?: boolean;
  refetchInterval?: number;
  onSuccess?: (data: T) => void;
  onError?: (error: Error) => void;
}

interface UseFetchReturn<T> {
  data: T | undefined;
  error: Error | null;
  isLoading: boolean;
  isError: boolean;
  refetch: () => Promise<void>;
}

function useFetch<T>(
  url: string,
  options: UseFetchOptions<T> = {}
): UseFetchReturn<T> {
  const { enabled = true, onSuccess, onError } = options;
  const [data, setData] = useState<T>();
  const [error, setError] = useState<Error | null>(null);
  const [isLoading, setIsLoading] = useState(false);

  const fetchData = useCallback(async () => {
    setIsLoading(true);
    setError(null);

    try {
      const response = await fetch(url);
      if (!response.ok) throw new Error(`HTTP ${response.status}`);
      const json = (await response.json()) as T;
      setData(json);
      onSuccess?.(json);
    } catch (err) {
      const error = err instanceof Error ? err : new Error(String(err));
      setError(error);
      onError?.(error);
    } finally {
      setIsLoading(false);
    }
  }, [url, onSuccess, onError]);

  useEffect(() => {
    if (enabled) fetchData();
  }, [enabled, fetchData]);

  return {
    data,
    error,
    isLoading,
    isError: error !== null,
    refetch: fetchData,
  };
}
```

#### 2.2.2 Next.js (App Router)

**Skill Level:** Expert | **Version:** 15.x

```
Next.js App Router Architecture
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
project-root/
├── src/
│   ├── app/                     # App Router
│   │   ├── (auth)/              # Route group (no URL segment)
│   │   │   ├── login/
│   │   │   │   └── page.tsx
│   │   │   ├── register/
│   │   │   │   └── page.tsx
│   │   │   └── layout.tsx       # Auth-specific layout
│   │   ├── (dashboard)/
│   │   │   ├── dashboard/
│   │   │   │   ├── page.tsx
│   │   │   │   ├── loading.tsx  # Loading UI
│   │   │   │   └── error.tsx    # Error boundary
│   │   │   ├── settings/
│   │   │   │   └── page.tsx
│   │   │   └── layout.tsx       # Dashboard layout w/ sidebar
│   │   ├── api/                 # API Routes
│   │   │   └── users/
│   │   │       └── route.ts
│   │   ├── layout.tsx           # Root layout
│   │   ├── page.tsx             # Home page
│   │   ├── not-found.tsx        # 404 page
│   │   ├── error.tsx            # Global error boundary
│   │   ├── global-error.tsx     # Root error boundary
│   │   └── globals.css
│   ├── components/
│   │   ├── ui/                  # Reusable UI primitives
│   │   │   ├── button.tsx
│   │   │   ├── input.tsx
│   │   │   ├── dialog.tsx
│   │   │   └── index.ts
│   │   ├── features/            # Feature-specific components
│   │   │   ├── auth/
│   │   │   └── dashboard/
│   │   └── layouts/             # Layout components
│   │       ├── header.tsx
│   │       ├── sidebar.tsx
│   │       └── footer.tsx
│   ├── lib/                     # Utility functions
│   │   ├── utils.ts
│   │   ├── constants.ts
│   │   └── validations.ts
│   ├── hooks/                   # Custom hooks
│   ├── stores/                  # State management
│   ├── services/                # API service layer
│   ├── types/                   # TypeScript types
│   └── styles/                  # Additional styles
├── public/                      # Static assets
├── tests/                       # Test files
├── next.config.ts
├── tailwind.config.ts
├── tsconfig.json
└── package.json
```

```tsx
// ============================================
// NEXT.JS SERVER COMPONENT (Default)
// ============================================
// app/(dashboard)/dashboard/page.tsx

import { Suspense } from 'react';
import { Metadata } from 'next';
import { getUserSession } from '@/lib/auth';
import { DashboardStats } from '@/components/features/dashboard/stats';
import { RecentActivity } from '@/components/features/dashboard/recent-activity';
import { DashboardSkeleton } from '@/components/features/dashboard/skeleton';

export const metadata: Metadata = {
  title: 'Dashboard | MyApp',
  description: 'View your dashboard analytics and recent activity.',
};

export default async function DashboardPage() {
  const session = await getUserSession();

  return (
    <div className="space-y-8">
      <header>
        <h1 className="text-3xl font-bold tracking-tight">
          Welcome back, {session.user.name}
        </h1>
        <p className="text-muted-foreground mt-1">
          Here's what's happening with your account today.
        </p>
      </header>

      {/* Streaming with Suspense */}
      <Suspense fallback={<DashboardSkeleton />}>
        <DashboardStats userId={session.user.id} />
      </Suspense>

      <Suspense fallback={<div className="animate-pulse h-64 bg-muted rounded-lg" />}>
        <RecentActivity userId={session.user.id} />
      </Suspense>
    </div>
  );
}

// ============================================
// SERVER ACTION
// ============================================
// app/actions/users.ts
'use server';

import { revalidatePath } from 'next/cache';
import { redirect } from 'next/navigation';
import { z } from 'zod';
import { db } from '@/lib/db';
import { getUserSession } from '@/lib/auth';

const UpdateProfileSchema = z.object({
  name: z.string().min(2).max(100),
  email: z.string().email(),
  bio: z.string().max(500).optional(),
});

export type UpdateProfileState = {
  errors?: Record<string, string[]>;
  message?: string;
  success?: boolean;
};

export async function updateProfile(
  prevState: UpdateProfileState,
  formData: FormData
): Promise<UpdateProfileState> {
  // 1. Authenticate
  const session = await getUserSession();
  if (!session) redirect('/login');

  // 2. Validate
  const validatedFields = UpdateProfileSchema.safeParse({
    name: formData.get('name'),
    email: formData.get('email'),
    bio: formData.get('bio'),
  });

  if (!validatedFields.success) {
    return {
      errors: validatedFields.error.flatten().fieldErrors,
      message: 'Validation failed. Please check the form fields.',
    };
  }

  // 3. Mutate
  try {
    await db.user.update({
      where: { id: session.user.id },
      data: validatedFields.data,
    });
  } catch (error) {
    return {
      message: 'Database error: Failed to update profile.',
    };
  }

  // 4. Revalidate & return
  revalidatePath('/settings');
  return { success: true, message: 'Profile updated successfully.' };
}

// ============================================
// CLIENT COMPONENT (using Server Action)
// ============================================
// components/features/settings/profile-form.tsx
'use client';

import { useActionState } from 'react';
import { updateProfile, type UpdateProfileState } from '@/app/actions/users';
import { Button } from '@/components/ui/button';
import { Input } from '@/components/ui/input';

interface ProfileFormProps {
  user: { name: string; email: string; bio?: string };
}

export function ProfileForm({ user }: ProfileFormProps) {
  const initialState: UpdateProfileState = { message: '' };
  const [state, formAction, isPending] = useActionState(
    updateProfile,
    initialState
  );

  return (
    <form action={formAction} className="space-y-6 max-w-lg">
      <div>
        <label htmlFor="name" className="block text-sm font-medium">
          Name
        </label>
        <Input
          id="name"
          name="name"
          defaultValue={user.name}
          aria-describedby="name-error"
        />
        {state.errors?.name && (
          <p id="name-error" className="text-sm text-red-500 mt-1">
            {state.errors.name[0]}
          </p>
        )}
      </div>

      <div>
        <label htmlFor="email" className="block text-sm font-medium">
          Email
        </label>
        <Input
          id="email"
          name="email"
          type="email"
          defaultValue={user.email}
          aria-describedby="email-error"
        />
        {state.errors?.email && (
          <p id="email-error" className="text-sm text-red-500 mt-1">
            {state.errors.email[0]}
          </p>
        )}
      </div>

      <div>
        <label htmlFor="bio" className="block text-sm font-medium">
          Bio
        </label>
        <textarea
          id="bio"
          name="bio"
          defaultValue={user.bio}
          rows={3}
          className="w-full rounded-md border px-3 py-2"
          aria-describedby="bio-error"
        />
        {state.errors?.bio && (
          <p id="bio-error" className="text-sm text-red-500 mt-1">
            {state.errors.bio[0]}
          </p>
        )}
      </div>

      {state.message && (
        <div
          className={`p-3 rounded-md text-sm ${
            state.success
              ? 'bg-green-50 text-green-700'
              : 'bg-red-50 text-red-700'
          }`}
          role="alert"
        >
          {state.message}
        </div>
      )}

      <Button type="submit" isLoading={isPending}>
        Save Changes
      </Button>
    </form>
  );
}
```

#### 2.2.3 Vue.js

**Skill Level:** Advanced | **Version:** 3.x (Composition API)

```vue
<!-- ============================================
     VUE 3 COMPOSITION API — PRODUCTION PATTERN
     ============================================ -->
<script setup lang="ts">
import { ref, computed, watch, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import type { User } from '@/types';

// --- PROPS ---
interface Props {
  userId: string;
  showAvatar?: boolean;
}

const props = withDefaults(defineProps<Props>(), {
  showAvatar: true,
});

// --- EMITS ---
const emit = defineEmits<{
  'update:user': [user: User];
  'delete': [userId: string];
}>();

// --- STATE ---
const user = ref<User | null>(null);
const isLoading = ref(false);
const error = ref<string | null>(null);

// --- COMPUTED ---
const displayName = computed(() => {
  if (!user.value) return 'Unknown';
  return `${user.value.name} (${user.value.role})`;
});

// --- COMPOSABLE (Custom Hook equivalent) ---
function useUserApi() {
  async function fetchUser(id: string): Promise<User> {
    const response = await fetch(`/api/users/${id}`);
    if (!response.ok) throw new Error('Failed to fetch user');
    return response.json();
  }

  async function deleteUser(id: string): Promise<void> {
    const response = await fetch(`/api/users/${id}`, { method: 'DELETE' });
    if (!response.ok) throw new Error('Failed to delete user');
  }

  return { fetchUser, deleteUser };
}

const { fetchUser, deleteUser } = useUserApi();

// --- LIFECYCLE ---
onMounted(async () => {
  isLoading.value = true;
  try {
    user.value = await fetchUser(props.userId);
  } catch (err) {
    error.value = err instanceof Error ? err.message : 'Unknown error';
  } finally {
    isLoading.value = false;
  }
});

// --- METHODS ---
async function handleDelete() {
  if (!user.value) return;
  await deleteUser(user.value.id);
  emit('delete', user.value.id);
}
</script>

<template>
  <div class="user-card">
    <div v-if="isLoading" class="skeleton" aria-busy="true">Loading...</div>

    <div v-else-if="error" class="error" role="alert">
      {{ error }}
    </div>

    <template v-else-if="user">
      <img
        v-if="showAvatar"
        :src="user.avatar"
        :alt="`${user.name}'s avatar`"
        class="avatar"
        loading="lazy"
      />
      <h2>{{ displayName }}</h2>
      <p>{{ user.email }}</p>
      <button @click="handleDelete" class="btn-danger">
        Delete User
      </button>
    </template>
  </div>
</template>

<style scoped>
.user-card {
  padding: var(--space-4);
  border-radius: var(--radius-md);
  border: 1px solid var(--color-neutral-200);
}

.avatar {
  width: 64px;
  height: 64px;
  border-radius: var(--radius-full);
  object-fit: cover;
}
</style>
```

---

### 2.3 State Management

```
State Management Decision Tree
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Is the state from the server?
├── YES → Use TanStack Query / SWR
│         (caching, revalidation, background updates)
│
└── NO → Is it shared across multiple components?
    ├── NO → Use useState / useReducer (local state)
    │
    └── YES → How complex is the state?
        ├── SIMPLE (theme, auth) → Use Context API / Zustand
        ├── MEDIUM (form, filters) → Use Zustand / Jotai
        └── COMPLEX (large app, many devs) → Use Redux Toolkit
```

**Zustand Store (Recommended Default):**

```typescript
// stores/auth-store.ts
import { create } from 'zustand';
import { devtools, persist, subscribeWithSelector } from 'zustand/middleware';
import { immer } from 'zustand/middleware/immer';

interface User {
  id: string;
  name: string;
  email: string;
  role: 'admin' | 'user';
}

interface AuthState {
  user: User | null;
  token: string | null;
  isAuthenticated: boolean;
  isLoading: boolean;
}

interface AuthActions {
  login: (email: string, password: string) => Promise<void>;
  logout: () => void;
  updateUser: (updates: Partial<User>) => void;
  setLoading: (loading: boolean) => void;
}

type AuthStore = AuthState & AuthActions;

export const useAuthStore = create<AuthStore>()(
  devtools(
    persist(
      subscribeWithSelector(
        immer((set, get) => ({
          // --- STATE ---
          user: null,
          token: null,
          isAuthenticated: false,
          isLoading: false,

          // --- ACTIONS ---
          login: async (email, password) => {
            set((state) => { state.isLoading = true; });

            try {
              const response = await fetch('/api/auth/login', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ email, password }),
              });

              if (!response.ok) throw new Error('Login failed');

              const data = await response.json();

              set((state) => {
                state.user = data.user;
                state.token = data.token;
                state.isAuthenticated = true;
                state.isLoading = false;
              });
            } catch (error) {
              set((state) => { state.isLoading = false; });
              throw error;
            }
          },

          logout: () => {
            set((state) => {
              state.user = null;
              state.token = null;
              state.isAuthenticated = false;
            });
          },

          updateUser: (updates) => {
            set((state) => {
              if (state.user) {
                Object.assign(state.user, updates);
              }
            });
          },

          setLoading: (loading) => {
            set((state) => { state.isLoading = loading; });
          },
        }))
      ),
      {
        name: 'auth-storage',
        partialize: (state) => ({
          user: state.user,
          token: state.token,
          isAuthenticated: state.isAuthenticated,
        }),
      }
    ),
    { name: 'AuthStore' }
  )
);

// --- SELECTORS (for optimized re-renders) ---
export const selectUser = (state: AuthStore) => state.user;
export const selectIsAuthenticated = (state: AuthStore) => state.isAuthenticated;
export const selectIsAdmin = (state: AuthStore) => state.user?.role === 'admin';
```

---

### 2.4 Styling & UI Systems

**Tailwind CSS Configuration (Production):**

```typescript
// tailwind.config.ts
import type { Config } from 'tailwindcss';
import tailwindAnimate from 'tailwindcss-animate';

const config: Config = {
  darkMode: 'class',
  content: [
    './src/**/*.{ts,tsx,mdx}',
    './components/**/*.{ts,tsx}',
  ],
  theme: {
    container: {
      center: true,
      padding: '1rem',
      screens: {
        '2xl': '1400px',
      },
    },
    extend: {
      colors: {
        border: 'hsl(var(--border))',
        background: 'hsl(var(--background))',
        foreground: 'hsl(var(--foreground))',
        primary: {
          DEFAULT: 'hsl(var(--primary))',
          foreground: 'hsl(var(--primary-foreground))',
        },
        muted: {
          DEFAULT: 'hsl(var(--muted))',
          foreground: 'hsl(var(--muted-foreground))',
        },
        destructive: {
          DEFAULT: 'hsl(var(--destructive))',
          foreground: 'hsl(var(--destructive-foreground))',
        },
      },
      fontFamily: {
        sans: ['var(--font-inter)', 'system-ui', 'sans-serif'],
        mono: ['var(--font-jetbrains)', 'monospace'],
      },
      keyframes: {
        'fade-in': {
          from: { opacity: '0', transform: 'translateY(8px)' },
          to: { opacity: '1', transform: 'translateY(0)' },
        },
        'slide-in-right': {
          from: { transform: 'translateX(100%)' },
          to: { transform: 'translateX(0)' },
        },
      },
      animation: {
        'fade-in': 'fade-in 0.3s ease-out',
        'slide-in-right': 'slide-in-right 0.3s ease-out',
      },
    },
  },
  plugins: [tailwindAnimate],
};

export default config;
```

---

### 2.5 Performance Optimization

```
Frontend Performance Checklist
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Loading Performance
  ☐ Code splitting with dynamic imports
  ☐ Route-based lazy loading
  ☐ Image optimization (next/image, WebP/AVIF, lazy loading)
  ☐ Font optimization (font-display: swap, preload)
  ☐ Critical CSS inlined
  ☐ Tree shaking enabled
  ☐ Bundle analysis (webpack-bundle-analyzer)
  ☐ Compression (Brotli > gzip)

Runtime Performance
  ☐ React.memo for expensive components
  ☐ useMemo / useCallback for expensive computations
  ☐ Virtual scrolling for large lists (TanStack Virtual)
  ☐ Debounce/throttle user inputs
  ☐ Web Workers for heavy computation
  ☐ requestAnimationFrame for animations
  ☐ Avoid layout thrashing

Caching
  ☐ Service Workers for offline support
  ☐ HTTP Cache-Control headers properly configured
  ☐ Static asset fingerprinting (hash in filename)
  ☐ API response caching (TanStack Query staleTime)

Core Web Vitals Targets
  ☐ LCP (Largest Contentful Paint) < 2.5s
  ☐ INP (Interaction to Next Paint) < 200ms
  ☐ CLS (Cumulative Layout Shift) < 0.1
```

```tsx
// Performance Optimization Examples

// 1. Dynamic Import with Loading State
import dynamic from 'next/dynamic';

const HeavyChart = dynamic(
  () => import('@/components/features/analytics/chart'),
  {
    loading: () => <div className="h-64 animate-pulse bg-muted rounded-lg" />,
    ssr: false, // Client-only component
  }
);

// 2. Optimized Image Component
import Image from 'next/image';

function OptimizedHero() {
  return (
    <Image
      src="/hero.jpg"
      alt="Hero banner"
      width={1200}
      height={600}
      priority // Preloads LCP image
      sizes="(max-width: 768px) 100vw, (max-width: 1200px) 80vw, 1200px"
      className="rounded-lg object-cover"
    />
  );
}

// 3. Virtual List for Large Datasets
import { useVirtualizer } from '@tanstack/react-virtual';
import { useRef } from 'react';

function VirtualList({ items }: { items: string[] }) {
  const parentRef = useRef<HTMLDivElement>(null);

  const virtualizer = useVirtualizer({
    count: items.length,
    getScrollElement: () => parentRef.current,
    estimateSize: () => 48,
    overscan: 5,
  });

  return (
    <div ref={parentRef} className="h-[400px] overflow-auto">
      <div
        style={{ height: `${virtualizer.getTotalSize()}px`, position: 'relative' }}
      >
        {virtualizer.getVirtualItems().map((virtualItem) => (
          <div
            key={virtualItem.key}
            style={{
              position: 'absolute',
              top: 0,
              left: 0,
              width: '100%',
              height: `${virtualItem.size}px`,
              transform: `translateY(${virtualItem.start}px)`,
            }}
          >
            {items[virtualItem.index]}
          </div>
        ))}
      </div>
    </div>
  );
}
```

---

### 2.6 Accessibility (a11y)

```
WCAG 2.2 Compliance Checklist (Level AA)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Perceivable
  ☐ Alt text for all meaningful images
  ☐ Captions for video content
  ☐ Sufficient color contrast (4.5:1 text, 3:1 large text)
  ☐ Don't rely on color alone to convey information
  ☐ Responsive text (no horizontal scroll at 320px)
  ☐ Content reflows up to 400% zoom

Operable
  ☐ All functionality available via keyboard
  ☐ Visible focus indicators on all interactive elements
  ☐ No keyboard traps
  ☐ Skip navigation link
  ☐ Page titles are descriptive
  ☐ Focus order is logical
  ☐ Touch targets ≥ 24x24 CSS pixels

Understandable
  ☐ Language attribute set on <html>
  ☐ Form inputs have associated labels
  ☐ Error messages are clear and specific
  ☐ Consistent navigation patterns

Robust
  ☐ Valid HTML
  ☐ ARIA used correctly (prefer native HTML)
  ☐ Name, Role, Value for custom components
  ☐ Status messages use aria-live regions
```

```tsx
// Accessible Modal Component Example
'use client';

import { useEffect, useRef, type ReactNode } from 'react';
import { createPortal } from 'react-dom';

interface ModalProps {
  isOpen: boolean;
  onClose: () => void;
  title: string;
  children: ReactNode;
  description?: string;
}

export function Modal({ isOpen, onClose, title, description, children }: ModalProps) {
  const dialogRef = useRef<HTMLDialogElement>(null);
  const previousFocusRef = useRef<HTMLElement | null>(null);

  useEffect(() => {
    const dialog = dialogRef.current;
    if (!dialog) return;

    if (isOpen) {
      previousFocusRef.current = document.activeElement as HTMLElement;
      dialog.showModal();
    } else {
      dialog.close();
      previousFocusRef.current?.focus();
    }
  }, [isOpen]);

  useEffect(() => {
    const handleKeyDown = (e: KeyboardEvent) => {
      if (e.key === 'Escape') onClose();
    };

    if (isOpen) {
      document.addEventListener('keydown', handleKeyDown);
      return () => document.removeEventListener('keydown', handleKeyDown);
    }
  }, [isOpen, onClose]);

  if (!isOpen) return null;

  return createPortal(
    <dialog
      ref={dialogRef}
      className="backdrop:bg-black/50 rounded-lg p-0 max-w-lg w-full"
      aria-labelledby="modal-title"
      aria-describedby={description ? 'modal-description' : undefined}
      onClick={(e) => {
        // Close on backdrop click
        if (e.target === dialogRef.current) onClose();
      }}
    >
      <div className="p-6" role="document">
        <header className="flex items-center justify-between mb-4">
          <h2 id="modal-title" className="text-lg font-semibold">
            {title}
          </h2>
          <button
            onClick={onClose}
            aria-label="Close dialog"
            className="rounded-full p-1 hover:bg-neutral-100"
          >
            ✕
          </button>
        </header>

        {description && (
          <p id="modal-description" className="text-sm text-muted-foreground mb-4">
            {description}
          </p>
        )}

        <div>{children}</div>
      </div>
    </dialog>,
    document.body
  );
}
```

---

### 2.7 Testing (Frontend)

```typescript
// ============================================
// FRONTEND TESTING STRATEGY
// ============================================

// Testing Pyramid:
// ┌─────────┐
// │   E2E   │  ← Few (critical user journeys)
// │ (Playwright)
// ├─────────┤
// │  Integ. │  ← Some (component interactions)
// │ (Testing Library)
// ├─────────┤
// │  Unit   │  ← Many (pure functions, hooks)
// │ (Vitest)│
// └─────────┘

// --- UNIT TEST (Vitest) ---
// lib/__tests__/format.test.ts
import { describe, it, expect } from 'vitest';
import { formatCurrency, formatDate, truncate } from '../format';

describe('formatCurrency', () => {
  it('formats USD correctly', () => {
    expect(formatCurrency(1234.56, 'USD')).toBe('$1,234.56');
  });

  it('handles zero', () => {
    expect(formatCurrency(0, 'USD')).toBe('$0.00');
  });

  it('handles negative values', () => {
    expect(formatCurrency(-42.5, 'USD')).toBe('-$42.50');
  });
});

describe('truncate', () => {
  it('truncates long strings', () => {
    expect(truncate('Hello, World!', 5)).toBe('Hello...');
  });

  it('does not truncate short strings', () => {
    expect(truncate('Hi', 10)).toBe('Hi');
  });
});

// --- COMPONENT TEST (Testing Library + Vitest) ---
// components/__tests__/button.test.tsx
import { render, screen } from '@testing-library/react';
import userEvent from '@testing-library/user-event';
import { describe, it, expect, vi } from 'vitest';
import { Button } from '../ui/button';

describe('Button', () => {
  it('renders with correct text', () => {
    render(<Button>Click me</Button>);
    expect(screen.getByRole('button', { name: /click me/i })).toBeInTheDocument();
  });

  it('calls onClick handler when clicked', async () => {
    const user = userEvent.setup();
    const handleClick = vi.fn();

    render(<Button onClick={handleClick}>Click me</Button>);
    await user.click(screen.getByRole('button'));

    expect(handleClick).toHaveBeenCalledTimes(1);
  });

  it('shows loading state and disables button', () => {
    render(<Button isLoading>Submit</Button>);
    const button = screen.getByRole('button');

    expect(button).toBeDisabled();
    expect(button).toHaveAttribute('aria-busy', 'true');
  });

  it('applies variant classes correctly', () => {
    render(<Button variant="destructive">Delete</Button>);
    const button = screen.getByRole('button');

    expect(button).toHaveClass('bg-red-600');
  });
});

// --- E2E TEST (Playwright) ---
// tests/e2e/auth.spec.ts
import { test, expect } from '@playwright/test';

test.describe('Authentication Flow', () => {
  test('user can log in successfully', async ({ page }) => {
    await page.goto('/login');

    await page.getByLabel('Email').fill('user@example.com');
    await page.getByLabel('Password').fill('securepassword123');
    await page.getByRole('button', { name: /sign in/i }).click();

    // Should redirect to dashboard
    await expect(page).toHaveURL('/dashboard');
    await expect(page.getByRole('heading', { name: /welcome back/i })).toBeVisible();
  });

  test('shows validation errors for invalid input', async ({ page }) => {
    await page.goto('/login');

    await page.getByRole('button', { name: /sign in/i }).click();

    await expect(page.getByText(/email is required/i)).toBeVisible();
    await expect(page.getByText(/password is required/i)).toBeVisible();
  });

  test('shows error for invalid credentials', async ({ page }) => {
    await page.goto('/login');

    await page.getByLabel('Email').fill('wrong@example.com');
    await page.getByLabel('Password').fill('wrongpassword');
    await page.getByRole('button', { name: /sign in/i }).click();

    await expect(page.getByRole('alert')).toContainText(/invalid credentials/i);
  });
});
```

---

## 3. Backend Development

### 3.1 Server-Side Languages & Runtimes

```
Language Selection Matrix
━━━━━━━━━━━━━━━━━━━━━━━━━
┌─────────────┬──────────┬──────────────┬───────────────┬────────────┐
│  Language   │  Speed   │  Ecosystem   │  Best For     │  Agent     │
│             │          │              │               │  Default?  │
├─────────────┼──────────┼──────────────┼───────────────┼────────────┤
│ TypeScript  │ ●●●○○    │ ●●●●●        │ Full-stack,   │ ✅ YES     │
│ (Node.js)   │          │              │ APIs, BFFs    │            │
├─────────────┼──────────┼──────────────┼───────────────┼────────────┤
│ Python      │ ●●○○○    │ ●●●●●        │ ML/AI, Data,  │ Situational│
│             │          │              │ Scripts, APIs │            │
├─────────────┼──────────┼──────────────┼───────────────┼────────────┤
│ Go          │ ●●●●●    │ ●●●○○        │ Microservices,│ Situational│
│             │          │              │ CLIs, Infra   │            │
├─────────────┼──────────┼──────────────┼───────────────┼────────────┤
│ Rust        │ ●●●●●    │ ●●●○○        │ Systems,      │ Situational│
│             │          │              │ Performance   │            │
├─────────────┼──────────┼──────────────┼───────────────┼────────────┤
│ Java/Kotlin │ ●●●●○    │ ●●●●●        │ Enterprise,   │ Situational│
│             │          │              │ Android       │            │
└─────────────┴──────────┴──────────────┴───────────────┴────────────┘
```

### 3.2 Backend Frameworks

#### 3.2.1 Node.js / TypeScript Frameworks

```
Framework Selection
━━━━━━━━━━━━━━━━━━━

REST API (simple → complex):
  1. Hono        → Ultra-fast, edge-native, lightweight
  2. Fastify     → High performance, schema-based validation
  3. Express     → Mature, massive ecosystem (legacy preference)
  4. NestJS      → Enterprise, Angular-style architecture

Full-Stack:
  1. Next.js     → React + API routes + SSR/SSG
  2. Remix       → React + progressive enhancement
  3. Nuxt        → Vue equivalent

Real-Time:
  1. Socket.io   → WebSockets with fallback
  2. ws          → Raw WebSocket library
  3. Hono + SSE  → Server-Sent Events

GraphQL:
  1. Apollo Server
  2. Yoga + Pothos
  3. tRPC        → End-to-end type-safe (recommended for TS full-stack)
```

#### 3.2.2 Production Express/Hono API

```typescript
// ============================================
// PRODUCTION API — HONO FRAMEWORK
// ============================================
// src/index.ts

import { Hono } from 'hono';
import { cors } from 'hono/cors';
import { logger } from 'hono/logger';
import { secureHeaders } from 'hono/secure-headers';
import { rateLimiter } from 'hono-rate-limiter';
import { prettyJSON } from 'hono/pretty-json';
import { HTTPException } from 'hono/http-exception';

import { authMiddleware } from './middleware/auth';
import { usersRouter } from './routes/users';
import { postsRouter } from './routes/posts';
import { healthRouter } from './routes/health';

import type { Env } from './types/env';

// --- APP INITIALIZATION ---
const app = new Hono<{ Bindings: Env }>();

// --- GLOBAL MIDDLEWARE ---
app.use('*', logger());
app.use('*', secureHeaders());
app.use('*', prettyJSON());

app.use('*', cors({
  origin: (origin) => {
    const allowedOrigins = ['https://myapp.com', 'https://www.myapp.com'];
    if (process.env.NODE_ENV === 'development') {
      allowedOrigins.push('http://localhost:3000');
    }
    return allowedOrigins.includes(origin) ? origin : '';
  },
  allowMethods: ['GET', 'POST', 'PUT', 'PATCH', 'DELETE', 'OPTIONS'],
  allowHeaders: ['Content-Type', 'Authorization'],
  credentials: true,
  maxAge: 86400,
}));

// Rate limiting
app.use('/api/*', rateLimiter({
  windowMs: 15 * 60 * 1000, // 15 minutes
  limit: 100,
  standardHeaders: 'draft-7',
  keyGenerator: (c) => c.req.header('x-forwarded-for') || 'unknown',
}));

// --- ROUTES ---
app.route('/api/health', healthRouter);
app.route('/api/users', usersRouter);
app.route('/api/posts', postsRouter);

// --- GLOBAL ERROR HANDLER ---
app.onError((err, c) => {
  console.error(`[Error] ${err.message}`, {
    stack: err.stack,
    url: c.req.url,
    method: c.req.method,
  });

  if (err instanceof HTTPException) {
    return c.json(
      {
        error: {
          message: err.message,
          status: err.status,
        },
      },
      err.status
    );
  }

  // Don't leak internal errors in production
  const message =
    process.env.NODE_ENV === 'production'
      ? 'Internal Server Error'
      : err.message;

  return c.json(
    {
      error: {
        message,
        status: 500,
      },
    },
    500
  );
});

// --- 404 HANDLER ---
app.notFound((c) => {
  return c.json(
    {
      error: {
        message: `Route not found: ${c.req.method} ${c.req.path}`,
        status: 404,
      },
    },
    404
  );
});

export default app;


// ============================================
// ROUTE MODULE — USERS
// ============================================
// src/routes/users.ts

import { Hono } from 'hono';
import { zValidator } from '@hono/zod-validator';
import { z } from 'zod';
import { authMiddleware, requireRole } from '../middleware/auth';
import { UserService } from '../services/user.service';
import type { Env } from '../types/env';

const usersRouter = new Hono<{ Bindings: Env }>();
const userService = new UserService();

// --- VALIDATION SCHEMAS ---
const CreateUserSchema = z.object({
  name: z.string().min(2).max(100).trim(),
  email: z.string().email().toLowerCase(),
  password: z.string().min(8).max(128).regex(
    /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*])/,
    'Password must contain uppercase, lowercase, number, and special character'
  ),
  role: z.enum(['admin', 'editor', 'viewer']).default('viewer'),
});

const UpdateUserSchema = CreateUserSchema.partial().omit({ password: true });

const QuerySchema = z.object({
  page: z.coerce.number().int().positive().default(1),
  limit: z.coerce.number().int().min(1).max(100).default(20),
  search: z.string().optional(),
  role: z.enum(['admin', 'editor', 'viewer']).optional(),
  sortBy: z.enum(['name', 'email', 'createdAt']).default('createdAt'),
  sortOrder: z.enum(['asc', 'desc']).default('desc'),
});

const ParamsSchema = z.object({
  id: z.string().uuid('Invalid user ID format'),
});

// --- ROUTES ---

// GET /api/users
usersRouter.get(
  '/',
  authMiddleware,
  zValidator('query', QuerySchema),
  async (c) => {
    const query = c.req.valid('query');

    const result = await userService.findMany({
      page: query.page,
      limit: query.limit,
      search: query.search,
      role: query.role,
      sortBy: query.sortBy,
      sortOrder: query.sortOrder,
    });

    return c.json({
      data: result.users,
      pagination: {
        page: query.page,
        limit: query.limit,
        total: result.total,
        totalPages: Math.ceil(result.total / query.limit),
        hasNext: query.page * query.limit < result.total,
        hasPrev: query.page > 1,
      },
    });
  }
);

// GET /api/users/:id
usersRouter.get(
  '/:id',
  authMiddleware,
  zValidator('param', ParamsSchema),
  async (c) => {
    const { id } = c.req.valid('param');
    const user = await userService.findById(id);

    if (!user) {
      return c.json({ error: { message: 'User not found', status: 404 } }, 404);
    }

    return c.json({ data: user });
  }
);

// POST /api/users
usersRouter.post(
  '/',
  authMiddleware,
  requireRole('admin'),
  zValidator('json', CreateUserSchema),
  async (c) => {
    const body = c.req.valid('json');

    const existingUser = await userService.findByEmail(body.email);
    if (existingUser) {
      return c.json(
        { error: { message: 'Email already in use', status: 409 } },
        409
      );
    }

    const user = await userService.create(body);

    return c.json({ data: user }, 201);
  }
);

// PATCH /api/users/:id
usersRouter.patch(
  '/:id',
  authMiddleware,
  zValidator('param', ParamsSchema),
  zValidator('json', UpdateUserSchema),
  async (c) => {
    const { id } = c.req.valid('param');
    const body = c.req.valid('json');

    const user = await userService.update(id, body);

    if (!user) {
      return c.json({ error: { message: 'User not found', status: 404 } }, 404);
    }

    return c.json({ data: user });
  }
);

// DELETE /api/users/:id
usersRouter.delete(
  '/:id',
  authMiddleware,
  requireRole('admin'),
  zValidator('param', ParamsSchema),
  async (c) => {
    const { id } = c.req.valid('param');

    const deleted = await userService.delete(id);

    if (!deleted) {
      return c.json({ error: { message: 'User not found', status: 404 } }, 404);
    }

    return c.json(null, 204);
  }
);

export { usersRouter };


// ============================================
// SERVICE LAYER — BUSINESS LOGIC
// ============================================
// src/services/user.service.ts

import { db } from '../lib/db';
import { hashPassword } from '../lib/crypto';
import type { User, CreateUserInput, UpdateUserInput, PaginationQuery } from '../types';

export class UserService {
  async findMany(query: PaginationQuery) {
    const { page, limit, search, role, sortBy, sortOrder } = query;
    const offset = (page - 1) * limit;

    const where: Record<string, unknown> = {};

    if (search) {
      where.OR = [
        { name: { contains: search, mode: 'insensitive' } },
        { email: { contains: search, mode: 'insensitive' } },
      ];
    }

    if (role) {
      where.role = role;
    }

    const [users, total] = await Promise.all([
      db.user.findMany({
        where,
        orderBy: { [sortBy]: sortOrder },
        skip: offset,
        take: limit,
        select: {
          id: true,
          name: true,
          email: true,
          role: true,
          createdAt: true,
          updatedAt: true,
          // Never select password
        },
      }),
      db.user.count({ where }),
    ]);

    return { users, total };
  }

  async findById(id: string): Promise<User | null> {
    return db.user.findUnique({
      where: { id },
      select: {
        id: true,
        name: true,
        email: true,
        role: true,
        createdAt: true,
        updatedAt: true,
      },
    });
  }

  async findByEmail(email: string): Promise<User | null> {
    return db.user.findUnique({
      where: { email },
    });
  }

  async create(input: CreateUserInput): Promise<User> {
    const hashedPassword = await hashPassword(input.password);

    return db.user.create({
      data: {
        ...input,
        password: hashedPassword,
      },
      select: {
        id: true,
        name: true,
        email: true,
        role: true,
        createdAt: true,
        updatedAt: true,
      },
    });
  }

  async update(id: string, input: UpdateUserInput): Promise<User | null> {
    try {
      return await db.user.update({
        where: { id },
        data: {
          ...input,
          updatedAt: new Date(),
        },
        select: {
          id: true,
          name: true,
          email: true,
          role: true,
          createdAt: true,
          updatedAt: true,
        },
      });
    } catch {
      return null; // Not found
    }
  }

  async delete(id: string): Promise<boolean> {
    try {
      await db.user.delete({ where: { id } });
      return true;
    } catch {
      return false;
    }
  }
}
```

---

### 3.3 API Design & Architecture

#### 3.3.1 REST API Standards

```
REST API Design Conventions
━━━━━━━━━━━━━━━━━━━━━━━━━━━

URL Structure:
  ✅ /api/v1/users              → Collection
  ✅ /api/v1/users/:id          → Single resource
  ✅ /api/v1/users/:id/posts    → Sub-resource
  ❌ /api/v1/getUsers           → Don't use verbs
  ❌ /api/v1/user               → Always plural

HTTP Methods:
  GET     → Read (safe, idempotent)
  POST    → Create (not idempotent)
  PUT     → Full replace (idempotent)
  PATCH   → Partial update (idempotent)
  DELETE  → Remove (idempotent)

Status Codes:
  200 OK                → Successful GET/PATCH/PUT
  201 Created           → Successful POST
  204 No Content        → Successful DELETE
  301 Moved Permanently → Permanent redirect
  304 Not Modified      → Cached response valid
  400 Bad Request       → Validation error
  401 Unauthorized      → No/invalid authentication
  403 Forbidden         → Authenticated but not authorized
  404 Not Found         → Resource doesn't exist
  409 Conflict          → Duplicate/conflicting state
  422 Unprocessable     → Semantically invalid
  429 Too Many Requests → Rate limit exceeded
  500 Internal Error    → Server error (never expose details)
  503 Service Unavail.  → Temporary outage
```

**Standard API Response Format:**

```typescript
// --- SUCCESS RESPONSE ---
interface ApiSuccessResponse<T> {
  data: T;
  pagination?: PaginationMeta; // For list endpoints
}

interface PaginationMeta {
  page: number;
  limit: number;
  total: number;
  totalPages: number;
  hasNext: boolean;
  hasPrev: boolean;
}

// Example:
{
  "data": [
    { "id": "1", "name": "Alice", "email": "alice@example.com" },
    { "id": "2", "name": "Bob", "email": "bob@example.com" }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 42,
    "totalPages": 3,
    "hasNext": true,
    "hasPrev": false
  }
}

// --- ERROR RESPONSE ---
interface ApiErrorResponse {
  error: {
    message: string;
    status: number;
    code?: string;           // Machine-readable error code
    details?: ValidationError[];  // Field-level errors
    requestId?: string;      // For debugging/support
  };
}

interface ValidationError {
  field: string;
  message: string;
  code: string;
}

// Example:
{
  "error": {
    "message": "Validation failed",
    "status": 400,
    "code": "VALIDATION_ERROR",
    "details": [
      { "field": "email", "message": "Invalid email format", "code": "invalid_string" },
      { "field": "password", "message": "Must be at least 8 characters", "code": "too_small" }
    ],
    "requestId": "req_abc123"
  }
}
```

#### 3.3.2 tRPC — End-to-End Type Safety

```typescript
// ============================================
// tRPC — FULL TYPE-SAFE API
// ============================================
// server/trpc/router.ts

import { initTRPC, TRPCError } from '@trpc/server';
import superjson from 'superjson';
import { z } from 'zod';
import type { Context } from './context';

const t = initTRPC.context<Context>().create({
  transformer: superjson,
  errorFormatter({ shape, error }) {
    return {
      ...shape,
      data: {
        ...shape.data,
        zodError:
          error.cause instanceof z.ZodError
            ? error.cause.flatten()
            : null,
      },
    };
  },
});

// Middleware
const isAuthenticated = t.middleware(({ ctx, next }) => {
  if (!ctx.session?.user) {
    throw new TRPCError({ code: 'UNAUTHORIZED' });
  }
  return next({
    ctx: {
      ...ctx,
      user: ctx.session.user,
    },
  });
});

const isAdmin = t.middleware(({ ctx, next }) => {
  if (ctx.session?.user?.role !== 'admin') {
    throw new TRPCError({ code: 'FORBIDDEN' });
  }
  return next({ ctx });
});

// Procedures
const publicProcedure = t.procedure;
const protectedProcedure = t.procedure.use(isAuthenticated);
const adminProcedure = t.procedure.use(isAuthenticated).use(isAdmin);

// Router
export const appRouter = t.router({
  users: t.router({
    list: protectedProcedure
      .input(z.object({
        page: z.number().int().positive().default(1),
        limit: z.number().int().min(1).max(100).default(20),
        search: z.string().optional(),
      }))
      .query(async ({ ctx, input }) => {
        const users = await ctx.db.user.findMany({
          skip: (input.page - 1) * input.limit,
          take: input.limit,
          where: input.search
            ? { name: { contains: input.search, mode: 'insensitive' } }
            : undefined,
        });
        const total = await ctx.db.user.count();
        return { users, total };
      }),

    byId: protectedProcedure
      .input(z.object({ id: z.string().uuid() }))
      .query(async ({ ctx, input }) => {
        const user = await ctx.db.user.findUnique({
          where: { id: input.id },
        });
        if (!user) throw new TRPCError({ code: 'NOT_FOUND' });
        return user;
      }),

    create: adminProcedure
      .input(z.object({
        name: z.string().min(2),
        email: z.string().email(),
        role: z.enum(['admin', 'editor', 'viewer']),
      }))
      .mutation(async ({ ctx, input }) => {
        return ctx.db.user.create({ data: input });
      }),

    delete: adminProcedure
      .input(z.object({ id: z.string().uuid() }))
      .mutation(async ({ ctx, input }) => {
        await ctx.db.user.delete({ where: { id: input.id } });
        return { success: true };
      }),
  }),
});

export type AppRouter = typeof appRouter;

// ============================================
// CLIENT USAGE (Fully Type-Safe!)
// ============================================
// On the frontend:
//
// const { data } = trpc.users.list.useQuery({ page: 1, limit: 10 });
// const createUser = trpc.users.create.useMutation();
// await createUser.mutateAsync({ name: "Alice", email: "alice@x.com", role: "editor" });
```

---

### 3.4 Database Design & Management

#### 3.4.1 Database Selection

```
Database Decision Matrix
━━━━━━━━━━━━━━━━━━━━━━━━

┌───────────────┬────────────┬──────────────────────────┬────────────────────┐
│   Database    │   Type     │   Best For               │   ORM/Driver       │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ PostgreSQL    │ Relational │ Complex queries, ACID,   │ Prisma, Drizzle    │
│               │            │ JSON, Full-text search   │                    │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ MySQL         │ Relational │ Read-heavy workloads,    │ Prisma, Drizzle    │
│               │            │ Replication              │                    │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ SQLite        │ Relational │ Embedded, edge, small    │ Drizzle, better-   │
│               │            │ apps, prototyping        │ sqlite3            │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ MongoDB       │ Document   │ Flexible schemas,        │ Mongoose, native   │
│               │            │ rapid prototyping        │ driver             │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ Redis         │ Key-Value  │ Caching, sessions,       │ ioredis            │
│               │            │ rate limiting, queues    │                    │
├───────────────┼────────────┼──────────────────────────┼────────────────────┤
│ Supabase      │ PostgreSQL │ BaaS, real-time,         │ Supabase client    │
│               │ + Auth     │ auth, storage            │                    │
└───────────────┴────────────┴──────────────────────────┴────────────────────┘

Default Recommendation: PostgreSQL + Drizzle ORM (or Prisma)
```

#### 3.4.2 Prisma Schema (Production)

```prisma
// prisma/schema.prisma

generator client {
  provider        = "prisma-client-js"
  previewFeatures = ["fullTextSearch", "fullTextIndex"]
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

// ── ENUMS ───────────────────────────────────────
enum UserRole {
  ADMIN
  EDITOR
  VIEWER
}

enum PostStatus {
  DRAFT
  PUBLISHED
  ARCHIVED
}

// ── MODELS ──────────────────────────────────────
model User {
  id            String    @id @default(cuid())
  email         String    @unique
  name          String
  passwordHash  String    @map("password_hash")
  role          UserRole  @default(VIEWER)
  avatarUrl     String?   @map("avatar_url")
  emailVerified Boolean   @default(false) @map("email_verified")
  lastLoginAt   DateTime? @map("last_login_at")

  // Relations
  posts         Post[]
  comments      Comment[]
  sessions      Session[]

  // Timestamps
  createdAt     DateTime  @default(now()) @map("created_at")
  updatedAt     DateTime  @updatedAt @map("updated_at")
  deletedAt     DateTime? @map("deleted_at") // Soft delete

  // Indexes
  @@index([email])
  @@index([role])
  @@index([createdAt])
  @@map("users")
}

model Post {
  id          String     @id @default(cuid())
  title       String
  slug        String     @unique
  content     String     @db.Text
  excerpt     String?
  status      PostStatus @default(DRAFT)
  publishedAt DateTime?  @map("published_at")

  // Relations
  author      User       @relation(fields: [authorId], references: [id], onDelete: Cascade)
  authorId    String     @map("author_id")
  comments    Comment[]
  tags        Tag[]

  // Timestamps
  createdAt   DateTime   @default(now()) @map("created_at")
  updatedAt   DateTime   @updatedAt @map("updated_at")

  // Indexes
  @@index([authorId])
  @@index([status])
  @@index([slug])
  @@index([publishedAt])
  @@map("posts")
}

model Comment {
  id        String   @id @default(cuid())
  content   String   @db.Text
  
  // Relations
  post      Post     @relation(fields: [postId], references: [id], onDelete: Cascade)
  postId    String   @map("post_id")
  author    User     @relation(fields: [authorId], references: [id], onDelete: Cascade)
  authorId  String   @map("author_id")
  parent    Comment? @relation("CommentReplies", fields: [parentId], references: [id])
  parentId  String?  @map("parent_id")
  replies   Comment[] @relation("CommentReplies")

  createdAt DateTime @default(now()) @map("created_at")
  updatedAt DateTime @updatedAt @map("updated_at")

  @@index([postId])
  @@index([authorId])
  @@map("comments")
}

model Tag {
  id    String @id @default(cuid())
  name  String @unique
  slug  String @unique
  posts Post[]

  @@map("tags")
}

model Session {
  id        String   @id @default(cuid())
  token     String   @unique
  expiresAt DateTime @map("expires_at")
  ipAddress String?  @map("ip_address")
  userAgent String?  @map("user_agent")

  user      User     @relation(fields: [userId], references: [id], onDelete: Cascade)
  userId    String   @map("user_id")

  createdAt DateTime @default(now()) @map("created_at")

  @@index([token])
  @@index([userId])
  @@map("sessions")
}
```

#### 3.4.3 Drizzle ORM (Alternative)

```typescript
// src/db/schema.ts
import {
  pgTable,
  text,
  varchar,
  timestamp,
  boolean,
  pgEnum,
  index,
  uniqueIndex,
} from 'drizzle-orm/pg-core';
import { relations } from 'drizzle-orm';
import { createId } from '@paralleldrive/cuid2';

// Enums
export const userRoleEnum = pgEnum('user_role', ['admin', 'editor', 'viewer']);
export const postStatusEnum = pgEnum('post_status', ['draft', 'published', 'archived']);

// Users table
export const users = pgTable('users', {
  id: text('id').primaryKey().$defaultFn(() => createId()),
  email: varchar('email', { length: 255 }).notNull().unique(),
  name: varchar('name', { length: 100 }).notNull(),
  passwordHash: text('password_hash').notNull(),
  role: userRoleEnum('role').default('viewer').notNull(),
  avatarUrl: text('avatar_url'),
  emailVerified: boolean('email_verified').default(false).notNull(),
  createdAt: timestamp('created_at').defaultNow().notNull(),
  updatedAt: timestamp('updated_at').defaultNow().notNull(),
}, (table) => ({
  emailIdx: uniqueIndex('users_email_idx').on(table.email),
  roleIdx: index('users_role_idx').on(table.role),
}));

// Posts table
export const posts = pgTable('posts', {
  id: text('id').primaryKey().$defaultFn(() => createId()),
  title: varchar('title', { length: 255 }).notNull(),
  slug: varchar('slug', { length: 255 }).notNull().unique(),
  content: text('content').notNull(),
  status: postStatusEnum('status').default('draft').notNull(),
  authorId: text('author_id').notNull().references(() => users.id, { onDelete: 'cascade' }),
  publishedAt: timestamp('published_at'),
  createdAt: timestamp('created_at').defaultNow().notNull(),
  updatedAt: timestamp('updated_at').defaultNow().notNull(),
}, (table) => ({
  slugIdx: uniqueIndex('posts_slug_idx').on(table.slug),
  authorIdx: index('posts_author_idx').on(table.authorId),
  statusIdx: index('posts_status_idx').on(table.status),
}));

// Relations
export const usersRelations = relations(users, ({ many }) => ({
  posts: many(posts),
}));

export const postsRelations = relations(posts, ({ one }) => ({
  author: one(users, {
    fields: [posts.authorId],
    references: [users.id],
  }),
}));
```

---

### 3.5 Authentication & Authorization

```typescript
// ============================================
// JWT + REFRESH TOKEN AUTH SYSTEM
// ============================================
// src/lib/auth.ts

import { SignJWT, jwtVerify, type JWTPayload } from 'jose';
import { hash, verify } from '@node-rs/argon2';

// --- CONFIGURATION ---
const ACCESS_TOKEN_SECRET = new TextEncoder().encode(process.env.JWT_ACCESS_SECRET!);
const REFRESH_TOKEN_SECRET = new TextEncoder().encode(process.env.JWT_REFRESH_SECRET!);
const ACCESS_TOKEN_EXPIRY = '15m';
const REFRESH_TOKEN_EXPIRY = '7d';

// --- TOKEN PAYLOAD ---
interface TokenPayload extends JWTPayload {
  userId: string;
  email: string;
  role: string;
}

// --- PASSWORD HASHING (Argon2id) ---
export async function hashPassword(password: string): Promise<string> {
  return hash(password, {
    memoryCost: 65536,    // 64 MB
    timeCost: 3,          // 3 iterations
    parallelism: 4,       // 4 threads
  });
}

export async function verifyPassword(
  hash: string,
  password: string
): Promise<boolean> {
  try {
    return await verify(hash, password);
  } catch {
    return false;
  }
}

// --- TOKEN GENERATION ---
export async function generateAccessToken(payload: Omit<TokenPayload, 'iat' | 'exp'>): Promise<string> {
  return new SignJWT(payload)
    .setProtectedHeader({ alg: 'HS256' })
    .setIssuedAt()
    .setExpirationTime(ACCESS_TOKEN_EXPIRY)
    .setIssuer('myapp')
    .setAudience('myapp-client')
    .sign(ACCESS_TOKEN_SECRET);
}

export async function generateRefreshToken(payload: Pick<TokenPayload, 'userId'>): Promise<string> {
  return new SignJWT(payload)
    .setProtectedHeader({ alg: 'HS256' })
    .setIssuedAt()
    .setExpirationTime(REFRESH_TOKEN_EXPIRY)
    .setIssuer('myapp')
    .sign(REFRESH_TOKEN_SECRET);
}

// --- TOKEN VERIFICATION ---
export async function verifyAccessToken(token: string): Promise<TokenPayload> {
  const { payload } = await jwtVerify(token, ACCESS_TOKEN_SECRET, {
    issuer: 'myapp',
    audience: 'myapp-client',
  });
  return payload as TokenPayload;
}

export async function verifyRefreshToken(token: string): Promise<TokenPayload> {
  const { payload } = await jwtVerify(token, REFRESH_TOKEN_SECRET, {
    issuer: 'myapp',
  });
  return payload as TokenPayload;
}

// --- AUTH MIDDLEWARE ---
// src/middleware/auth.ts

import { createMiddleware } from 'hono/factory';
import { HTTPException } from 'hono/http-exception';
import { verifyAccessToken } from '../lib/auth';

export const authMiddleware = createMiddleware(async (c, next) => {
  const authHeader = c.req.header('Authorization');

  if (!authHeader?.startsWith('Bearer ')) {
    throw new HTTPException(401, {
      message: 'Missing or invalid Authorization header',
    });
  }

  const token = authHeader.slice(7);

  try {
    const payload = await verifyAccessToken(token);
    c.set('user', payload);
  } catch (error) {
    throw new HTTPException(401, {
      message: 'Invalid or expired token',
    });
  }

  await next();
});

export function requireRole(...roles: string[]) {
  return createMiddleware(async (c, next) => {
    const user = c.get('user');

    if (!user || !roles.includes(user.role)) {
      throw new HTTPException(403, {
        message: 'Insufficient permissions',
      });
    }

    await next();
  });
}
```

---

### 3.6 Caching Strategies

```
Caching Strategy Guide
━━━━━━━━━━━━━━━━━━━━━━━

Layer 1: Browser Cache
  → Cache-Control headers
  → ETags for conditional requests
  → Service Workers for offline

Layer 2: CDN / Edge Cache
  → Static assets (immutable, max-age=31536000)
  → SSG pages (s-maxage, stale-while-revalidate)
  → API responses (varies by endpoint)

Layer 3: Application Cache (Redis)
  → Session data (TTL: 24h)
  → Computed results (TTL: varies)
  → Rate limiting counters (TTL: window size)
  → Queue messages

Layer 4: Database Query Cache
  → Materialized views
  → Query result caching
  → Connection pooling

Cache Invalidation Strategy:
  1. Time-based (TTL)           → Simple, eventual consistency
  2. Event-based (pub/sub)      → Real-time, more complex
  3. Version-based (cache keys) → Deterministic, key management
```

```typescript
// --- REDIS CACHING SERVICE ---
// src/lib/cache.ts

import Redis from 'ioredis';

const redis = new Redis(process.env.REDIS_URL!);

export class CacheService {
  private prefix: string;

  constructor(prefix = 'app') {
    this.prefix = prefix;
  }

  private key(key: string): string {
    return `${this.prefix}:${key}`;
  }

  async get<T>(key: string): Promise<T | null> {
    const data = await redis.get(this.key(key));
    if (!data) return null;
    return JSON.parse(data) as T;
  }

  async set<T>(key: string, value: T, ttlSeconds: number): Promise<void> {
    await redis.setex(this.key(key), ttlSeconds, JSON.stringify(value));
  }

  async del(key: string): Promise<void> {
    await redis.del(this.key(key));
  }

  async delPattern(pattern: string): Promise<void> {
    const keys = await redis.keys(this.key(pattern));
    if (keys.length > 0) {
      await redis.del(...keys);
    }
  }

  /**
   * Cache-aside pattern: get from cache, or compute and store
   */
  async getOrSet<T>(
    key: string,
    ttlSeconds: number,
    factory: () => Promise<T>
  ): Promise<T> {
    const cached = await this.get<T>(key);
    if (cached !== null) return cached;

    const fresh = await factory();
    await this.set(key, fresh, ttlSeconds);
    return fresh;
  }
}

// Usage:
const cache = new CacheService('users');

async function getUserById(id: string) {
  return cache.getOrSet(`user:${id}`, 300, async () => {
    return db.user.findUnique({ where: { id } });
  });
}
```

---

### 3.7 Testing (Backend)

```typescript
// ============================================
// BACKEND TESTING — COMPREHENSIVE STRATEGY
// ============================================

// --- UNIT TEST (Service Layer) ---
// src/services/__tests__/user.service.test.ts

import { describe, it, expect, beforeEach, vi } from 'vitest';
import { UserService } from '../user.service';
import { prismaMock } from '../../test/mocks/prisma';

vi.mock('../../lib/db', () => ({
  db: prismaMock,
}));

describe('UserService', () => {
  let service: UserService;

  beforeEach(() => {
    service = new UserService();
    vi.clearAllMocks();
  });

  describe('findById', () => {
    it('returns user when found', async () => {
      const mockUser = {
        id: 'user-1',
        name: 'Alice',
        email: 'alice@example.com',
        role: 'VIEWER' as const,
        createdAt: new Date(),
        updatedAt: new Date(),
      };

      prismaMock.user.findUnique.mockResolvedValue(mockUser);

      const result = await service.findById('user-1');

      expect(result).toEqual(mockUser);
      expect(prismaMock.user.findUnique).toHaveBeenCalledWith({
        where: { id: 'user-1' },
        select: expect.objectContaining({
          id: true,
          email: true,
          name: true,
        }),
      });
    });

    it('returns null when user not found', async () => {
      prismaMock.user.findUnique.mockResolvedValue(null);

      const result = await service.findById('nonexistent');

      expect(result).toBeNull();
    });
  });

  describe('create', () => {
    it('hashes password before storing', async () => {
      const input = {
        name: 'Bob',
        email: 'bob@example.com',
        password: 'SecureP@ss1',
        role: 'viewer' as const,
      };

      prismaMock.user.create.mockResolvedValue({
        id: 'user-2',
        ...input,
        createdAt: new Date(),
        updatedAt: new Date(),
      } as any);

      await service.create(input);

      expect(prismaMock.user.create).toHaveBeenCalledWith(
        expect.objectContaining({
          data: expect.objectContaining({
            email: 'bob@example.com',
            // Password should be hashed, not plain text
            password: expect.not.stringContaining('SecureP@ss1'),
          }),
        })
      );
    });
  });
});

// --- INTEGRATION TEST (API Routes) ---
// src/routes/__tests__/users.integration.test.ts

import { describe, it, expect, beforeAll, afterAll } from 'vitest';
import app from '../../index';

describe('Users API', () => {
  let authToken: string;

  beforeAll(async () => {
    // Setup: create test user and get token
    const res = await app.request('/api/auth/login', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        email: 'admin@test.com',
        password: 'testpassword',
      }),
    });
    const data = await res.json();
    authToken = data.token;
  });

  describe('GET /api/users', () => {
    it('returns paginated list of users', async () => {
      const res = await app.request('/api/users?page=1&limit=10', {
        headers: { Authorization: `Bearer ${authToken}` },
      });

      expect(res.status).toBe(200);

      const body = await res.json();
      expect(body.data).toBeInstanceOf(Array);
      expect(body.pagination).toMatchObject({
        page: 1,
        limit: 10,
        total: expect.any(Number),
      });
    });

    it('returns 401 without auth token', async () => {
      const res = await app.request('/api/users');

      expect(res.status).toBe(401);
    });
  });

  describe('POST /api/users', () => {
    it('returns 400 for invalid input', async () => {
      const res = await app.request('/api/users', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          Authorization: `Bearer ${authToken}`,
        },
        body: JSON.stringify({
          name: '',       // Too short
          email: 'invalid', // Not an email
        }),
      });

      expect(res.status).toBe(400);

      const body = await res.json();
      expect(body.error.details).toBeInstanceOf(Array);
    });
  });
});
```

---

## 4. Architecture & Design Patterns

### 4.1 Application Architecture Patterns

```
Architecture Selection Guide
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Small Project (1-3 devs, single service):
  → Monolith + Feature-based folder structure
  → Next.js full-stack

Medium Project (3-10 devs, moderate complexity):
  → Modular Monolith (domain-based modules)
  → Layered Architecture (Controller → Service → Repository)

Large Project (10+ devs, multiple teams):
  → Microservices with API Gateway
  → Event-Driven Architecture
  → CQRS for read/write optimization

Enterprise:
  → Domain-Driven Design (DDD)
  → Hexagonal Architecture (Ports & Adapters)
  → Event Sourcing
```

### 4.2 Layered Architecture

```
┌─────────────────────────────────────────────────┐
│                  PRESENTATION                    │
│     (Routes / Controllers / Handlers)            │
│     Validates input, returns responses           │
├─────────────────────────────────────────────────┤
│                    SERVICE                       │
│          (Business Logic Layer)                  │
│     Orchestrates operations, enforces rules      │
├─────────────────────────────────────────────────┤
│                  REPOSITORY                      │
│           (Data Access Layer)                    │
│     Database queries, external API calls         │
├─────────────────────────────────────────────────┤
│                   DATABASE                       │
│        (PostgreSQL, Redis, etc.)                 │
└─────────────────────────────────────────────────┘

Rules:
  • Each layer only depends on the layer below it
  • Never skip layers (Controller → Repository)
  • Business logic ONLY in Service layer
  • Controllers are thin — validate and delegate
  • Repositories are interchangeable (swap DB easily)
```

### 4.3 Common Design Patterns

```typescript
// ============================================
// DESIGN PATTERNS FOR WEB DEVELOPMENT
// ============================================

// --- 1. REPOSITORY PATTERN ---
interface IUserRepository {
  findById(id: string): Promise<User | null>;
  findMany(query: QueryOptions): Promise<User[]>;
  create(data: CreateUserInput): Promise<User>;
  update(id: string, data: UpdateUserInput): Promise<User>;
  delete(id: string): Promise<void>;
}

class PrismaUserRepository implements IUserRepository {
  constructor(private db: PrismaClient) {}

  async findById(id: string) {
    return this.db.user.findUnique({ where: { id } });
  }

  async findMany(query: QueryOptions) {
    return this.db.user.findMany({
      skip: query.offset,
      take: query.limit,
      orderBy: { [query.sortBy]: query.sortOrder },
    });
  }

  async create(data: CreateUserInput) {
    return this.db.user.create({ data });
  }

  async update(id: string, data: UpdateUserInput) {
    return this.db.user.update({ where: { id }, data });
  }

  async delete(id: string) {
    await this.db.user.delete({ where: { id } });
  }
}

// --- 2. STRATEGY PATTERN (Payment Processing) ---
interface PaymentStrategy {
  processPayment(amount: number, currency: string): Promise<PaymentResult>;
}

class StripePayment implements PaymentStrategy {
  async processPayment(amount: number, currency: string) {
    // Stripe-specific implementation
    return { success: true, transactionId: 'stripe_xxx' };
  }
}

class PayPalPayment implements PaymentStrategy {
  async processPayment(amount: number, currency: string) {
    // PayPal-specific implementation
    return { success: true, transactionId: 'paypal_xxx' };
  }
}

class PaymentService {
  constructor(private strategy: PaymentStrategy) {}

  setStrategy(strategy: PaymentStrategy) {
    this.strategy = strategy;
  }

  async pay(amount: number, currency: string) {
    return this.strategy.processPayment(amount, currency);
  }
}

// --- 3. OBSERVER PATTERN (Event Emitter) ---
type EventHandler<T = unknown> = (data: T) => void | Promise<void>;

class EventBus {
  private handlers = new Map<string, Set<EventHandler>>();

  on<T>(event: string, handler: EventHandler<T>): () => void {
    if (!this.handlers.has(event)) {
      this.handlers.set(event, new Set());
    }
    this.handlers.get(event)!.add(handler as EventHandler);

    // Return unsubscribe function
    return () => {
      this.handlers.get(event)?.delete(handler as EventHandler);
    };
  }

  async emit<T>(event: string, data: T): Promise<void> {
    const handlers = this.handlers.get(event);
    if (!handlers) return;

    await Promise.allSettled(
      Array.from(handlers).map((handler) => handler(data))
    );
  }
}

// Usage:
const eventBus = new EventBus();

eventBus.on<User>('user.created', async (user) => {
  await sendWelcomeEmail(user.email);
});

eventBus.on<User>('user.created', async (user) => {
  await createDefaultSettings(user.id);
});

// --- 4. MIDDLEWARE / CHAIN OF RESPONSIBILITY ---
type Middleware<T> = (context: T, next: () => Promise<void>) => Promise<void>;

class Pipeline<T> {
  private middlewares: Middleware<T>[] = [];

  use(middleware: Middleware<T>): this {
    this.middlewares.push(middleware);
    return this;
  }

  async execute(context: T): Promise<void> {
    let index = 0;

    const next = async (): Promise<void> => {
      if (index < this.middlewares.length) {
        const middleware = this.middlewares[index++];
        await middleware(context, next);
      }
    };

    await next();
  }
}
```

---

## 5. DevOps, CI/CD & Deployment

### 5.1 Docker Configuration

```dockerfile
# ============================================
# MULTI-STAGE DOCKERFILE — Node.js Production
# ============================================

# Stage 1: Dependencies
FROM node:22-alpine AS deps
WORKDIR /app

COPY package.json pnpm-lock.yaml ./
RUN corepack enable pnpm && pnpm install --frozen-lockfile

# Stage 2: Build
FROM node:22-alpine AS builder
WORKDIR /app

COPY --from=deps /app/node_modules ./node_modules
COPY . .

# Generate Prisma client
RUN npx prisma generate

# Build the application
RUN npm run build

# Stage 3: Production
FROM node:22-alpine AS runner
WORKDIR /app

# Security: run as non-root
RUN addgroup --system --gid 1001 nodejs
RUN adduser --system --uid 1001 appuser

# Copy only what's needed
COPY --from=builder --chown=appuser:nodejs /app/dist ./dist
COPY --from=builder --chown=appuser:nodejs /app/node_modules ./node_modules
COPY --from=builder --chown=appuser:nodejs /app/package.json ./
COPY --from=builder --chown=appuser:nodejs /app/prisma ./prisma

USER appuser

EXPOSE 3000

ENV NODE_ENV=production
ENV PORT=3000

HEALTHCHECK --interval=30s --timeout=3s --start-period=10s --retries=3 \
  CMD wget --quiet --tries=1 --spider http://localhost:3000/api/health || exit 1

CMD ["node", "dist/index.js"]
```

```yaml
# docker-compose.yml — Development
version: '3.9'

services:
  app:
    build:
      context: .
      dockerfile: Dockerfile
      target: builder
    ports:
      - '3000:3000'
    environment:
      DATABASE_URL: postgresql://postgres:postgres@db:5432/myapp
      REDIS_URL: redis://redis:6379
      NODE_ENV: development
    volumes:
      - .:/app
      - /app/node_modules
    depends_on:
      db:
        condition: service_healthy
      redis:
        condition: service_healthy
    command: npm run dev

  db:
    image: postgres:16-alpine
    ports:
      - '5432:5432'
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
      POSTGRES_DB: myapp
    volumes:
      - postgres_data:/var/lib/postgresql/data
    healthcheck:
      test: ['CMD-SHELL', 'pg_isready -U postgres']
      interval: 5s
      timeout: 5s
      retries: 5

  redis:
    image: redis:7-alpine
    ports:
      - '6379:6379'
    healthcheck:
      test: ['CMD', 'redis-cli', 'ping']
      interval: 5s
      timeout: 5s
      retries: 5

volumes:
  postgres_data:
```

### 5.2 GitHub Actions CI/CD

```yaml
# .github/workflows/ci.yml
name: CI/CD Pipeline

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true

env:
  NODE_VERSION: '22'
  PNPM_VERSION: '9'

jobs:
  # ── LINT & TYPE CHECK ─────────────────────
  quality:
    name: Code Quality
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: pnpm/action-setup@v4
        with:
          version: ${{ env.PNPM_VERSION }}

      - uses: actions/setup-node@v4
        with:
          node-version: ${{ env.NODE_VERSION }}
          cache: 'pnpm'

      - run: pnpm install --frozen-lockfile

      - name: TypeScript Type Check
        run: pnpm tsc --noEmit

      - name: Lint
        run: pnpm lint

      - name: Format Check
        run: pnpm format:check

  # ── UNIT & INTEGRATION TESTS ──────────────
  test:
    name: Tests
    runs-on: ubuntu-latest
    needs: quality

    services:
      postgres:
        image: postgres:16-alpine
        env:
          POSTGRES_USER: test
          POSTGRES_PASSWORD: test
          POSTGRES_DB: test
        ports:
          - 5432:5432
        options: >-
          --health-cmd pg_isready
          --health-interval 10s
          --health-timeout 5s
          --health-retries 5

    steps:
      - uses: actions/checkout@v4

      - uses: pnpm/action-setup@v4
        with:
          version: ${{ env.PNPM_VERSION }}

      - uses: actions/setup-node@v4
        with:
          node-version: ${{ env.NODE_VERSION }}
          cache: 'pnpm'

      - run: pnpm install --frozen-lockfile

      - name: Run database migrations
        run: pnpm prisma migrate deploy
        env:
          DATABASE_URL: postgresql://test:test@localhost:5432/test

      - name: Run tests
        run: pnpm test:ci
        env:
          DATABASE_URL: postgresql://test:test@localhost:5432/test

      - name: Upload coverage
        uses: codecov/codecov-action@v4
        with:
          files: ./coverage/lcov.info

  # ── E2E TESTS ─────────────────────────────
  e2e:
    name: E2E Tests
    runs-on: ubuntu-latest
    needs: quality
    steps:
      - uses: actions/checkout@v4

      - uses: pnpm/action-setup@v4
        with:
          version: ${{ env.PNPM_VERSION }}

      - uses: actions/setup-node@v4
        with:
          node-version: ${{ env.NODE_VERSION }}
          cache: 'pnpm'

      - run: pnpm install --frozen-lockfile
      - run: pnpm exec playwright install --with-deps chromium

      - name: Build
        run: pnpm build

      - name: Run E2E tests
        run: pnpm test:e2e

      - uses: actions/upload-artifact@v4
        if: failure()
        with:
          name: playwright-report
          path: playwright-report/

  # ── DEPLOY ─────────────────────────────────
  deploy:
    name: Deploy to Production
    runs-on: ubuntu-latest
    needs: [test, e2e]
    if: github.ref == 'refs/heads/main' && github.event_name == 'push'

    steps:
      - uses: actions/checkout@v4

      - name: Deploy to Vercel
        uses: amondnet/vercel-action@v25
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
          vercel-args: '--prod'
```

---

## 6. Security Best Practices

```
Security Checklist — MANDATORY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Input Validation & Sanitization
  ☐ Validate ALL user input (Zod schemas)
  ☐ Sanitize HTML output (DOMPurify)
  ☐ Parameterize database queries (NEVER string concat)
  ☐ Validate file uploads (type, size, extension)
  ☐ Limit request body size

Authentication
  ☐ Hash passwords with Argon2id (NOT bcrypt, NOT MD5)
  ☐ Implement rate limiting on auth endpoints
  ☐ Use short-lived access tokens (15min)
  ☐ Store refresh tokens securely (httpOnly cookies)
  ☐ Implement account lockout after failed attempts
  ☐ Force re-authentication for sensitive operations

Authorization
  ☐ Check permissions on EVERY protected endpoint
  ☐ Use RBAC or ABAC consistently
  ☐ Never trust client-side role checks alone
  ☐ Validate resource ownership (user can only access their data)

HTTP Security Headers
  ☐ Content-Security-Policy (CSP)
  ☐ Strict-Transport-Security (HSTS)
  ☐ X-Content-Type-Options: nosniff
  ☐ X-Frame-Options: DENY
  ☐ Referrer-Policy: strict-origin-when-cross-origin
  ☐ Permissions-Policy

Data Protection
  ☐ Encrypt data in transit (TLS 1.3)
  ☐ Encrypt sensitive data at rest
  ☐ Never log passwords, tokens, or PII
  ☐ Use environment variables for secrets
  ☐ Implement proper CORS configuration

Common Vulnerabilities (OWASP Top 10)
  ☐ SQL Injection       → Parameterized queries / ORM
  ☐ XSS                 → Output encoding, CSP
  ☐ CSRF                → CSRF tokens, SameSite cookies
  ☐ Broken Auth         → See authentication section
  ☐ SSRF                → Validate/whitelist URLs
  ☐ Mass Assignment     → Explicit field selection
  ☐ Insecure Deserialization → Validate before parsing
```

```typescript
// --- SECURITY HEADERS MIDDLEWARE ---
export function securityHeaders() {
  return createMiddleware(async (c, next) => {
    await next();

    c.header('X-Content-Type-Options', 'nosniff');
    c.header('X-Frame-Options', 'DENY');
    c.header('X-XSS-Protection', '0'); // Disabled (CSP preferred)
    c.header('Referrer-Policy', 'strict-origin-when-cross-origin');
    c.header('Permissions-Policy', 'camera=(), microphone=(), geolocation=()');
    c.header(
      'Strict-Transport-Security',
      'max-age=31536000; includeSubDomains; preload'
    );
    c.header(
      'Content-Security-Policy',
      [
        "default-src 'self'",
        "script-src 'self' 'unsafe-inline'",
        "style-src 'self' 'unsafe-inline'",
        "img-src 'self' data: https:",
        "font-src 'self'",
        "connect-src 'self'",
        "frame-ancestors 'none'",
        "base-uri 'self'",
        "form-action 'self'",
      ].join('; ')
    );
  });
}

// --- INPUT SANITIZATION ---
import DOMPurify from 'isomorphic-dompurify';

export function sanitizeHtml(dirty: string): string {
  return DOMPurify.sanitize(dirty, {
    ALLOWED_TAGS: ['b', 'i', 'em', 'strong', 'a', 'p', 'br', 'ul', 'ol', 'li'],
    ALLOWED_ATTR: ['href', 'target', 'rel'],
  });
}

// --- RATE LIMITER PER ROUTE ---
export function strictRateLimit(maxRequests: number, windowMs: number) {
  const store = new Map<string, { count: number; resetAt: number }>();

  return createMiddleware(async (c, next) => {
    const ip = c.req.header('x-forwarded-for') || 'unknown';
    const now = Date.now();
    const record = store.get(ip);

    if (!record || now > record.resetAt) {
      store.set(ip, { count: 1, resetAt: now + windowMs });
    } else if (record.count >= maxRequests) {
      c.header('Retry-After', String(Math.ceil((record.resetAt - now) / 1000)));
      return c.json(
        { error: { message: 'Too many requests', status: 429 } },
        429
      );
    } else {
      record.count++;
    }

    await next();
  });
}
```

---

## 7. Code Quality Standards

### 7.1 ESLint + Prettier Configuration

```javascript
// eslint.config.js (Flat Config — ESLint 9+)
import eslint from '@eslint/js';
import tseslint from 'typescript-eslint';
import react from 'eslint-plugin-react';
import reactHooks from 'eslint-plugin-react-hooks';
import jsxA11y from 'eslint-plugin-jsx-a11y';
import importPlugin from 'eslint-plugin-import';

export default tseslint.config(
  eslint.configs.recommended,
  ...tseslint.configs.strictTypeChecked,
  ...tseslint.configs.stylisticTypeChecked,
  {
    languageOptions: {
      parserOptions: {
        projectService: true,
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
  {
    plugins: {
      react,
      'react-hooks': reactHooks,
      'jsx-a11y': jsxA11y,
      import: importPlugin,
    },
    rules: {
      // TypeScript
      '@typescript-eslint/no-unused-vars': ['error', {
        argsIgnorePattern: '^_',
        varsIgnorePattern: '^_',
      }],
      '@typescript-eslint/no-explicit-any': 'error',
      '@typescript-eslint/prefer-nullish-coalescing': 'error',
      '@typescript-eslint/prefer-optional-chain': 'error',

      // React
      'react/jsx-no-target-blank': 'error',
      'react-hooks/rules-of-hooks': 'error',
      'react-hooks/exhaustive-deps': 'warn',

      // Accessibility
      'jsx-a11y/alt-text': 'error',
      'jsx-a11y/anchor-is-valid': 'error',
      'jsx-a11y/label-has-associated-control': 'error',

      // Imports
      'import/order': ['error', {
        groups: [
          'builtin',
          'external',
          'internal',
          'parent',
          'sibling',
          'index',
        ],
        'newlines-between': 'always',
        alphabetize: { order: 'asc' },
      }],
      'import/no-duplicates': 'error',
    },
  },
  {
    ignores: ['dist/', 'node_modules/', '.next/', 'coverage/'],
  }
);
```

```json
// .prettierrc
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 100,
  "bracketSpacing": true,
  "arrowParens": "always",
  "endOfLine": "lf",
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### 7.2 Git Conventions

```
Commit Message Format (Conventional Commits)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

<type>(<scope>): <short description>

<optional body — explain WHY, not WHAT>

<optional footer — breaking changes, issue refs>

Types:
  feat:     New feature
  fix:      Bug fix
  docs:     Documentation
  style:    Formatting (no code change)
  refactor: Code restructuring
  perf:     Performance improvement
  test:     Adding/updating tests
  chore:    Build/tooling/deps
  ci:       CI/CD changes
  revert:   Reverting a commit

Examples:
  feat(auth): add OAuth2 Google login
  fix(api): handle null user in GET /users/:id
  perf(db): add index on posts.published_at column
  refactor(components): extract Button variants to CVA

  BREAKING CHANGE: rename /api/users to /api/v2/accounts
```

---

## 8. Agent Behavior Rules & Decision Framework

### 8.1 Decision Trees

```
When Asked to Build a Feature:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. CLARIFY
   → What is the exact requirement?
   → What are the inputs and expected outputs?
   → Are there edge cases to consider?
   → What's the tech stack / existing codebase?

2. PLAN
   → Which architecture pattern fits?
   → What files need to be created/modified?
   → What are the dependencies?
   → What's the testing strategy?

3. IMPLEMENT
   → Write types/interfaces first
   → Implement business logic in service layer
   → Create API endpoints / UI components
   → Add validation (Zod schemas)
   → Add error handling

4. TEST
   → Write unit tests for business logic
   → Write integration tests for API
   → Write component tests for UI
   → Consider edge cases

5. DOCUMENT
   → Add JSDoc comments for public APIs
   → Update README if needed
   → Add migration notes if DB changes

Technology Selection Priority:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ALWAYS prefer:
  ✅ TypeScript over JavaScript
  ✅ Zod over manual validation
  ✅ Prisma/Drizzle over raw SQL (for apps)
  ✅ React Server Components over client-side fetching
  ✅ Tailwind CSS over custom CSS (unless design system exists)
  ✅ Vitest over Jest
  ✅ Playwright over Cypress
  ✅ pnpm over npm/yarn
  ✅ ESLint flat config over legacy config
  ✅ Server Actions over API routes (for form mutations in Next.js)
```

### 8.2 Code Generation Rules

```
Rule                              Priority    Description
────────────────────────────────────────────────────────────────────
Type everything                   CRITICAL    No 'any', no implicit types
Handle all errors                 CRITICAL    Every promise, every fetch
Validate all inputs               CRITICAL    Zod on API boundaries
Never expose secrets              CRITICAL    env vars, .env files
Use semantic HTML                 HIGH        Correct elements for purpose
Include ARIA when needed          HIGH        Especially custom components
Write pure functions              HIGH        Side effects explicit
Use early returns                 HIGH        Reduce nesting
Prefer composition over inherit.  HIGH        Flexible, testable code
Use const over let                MEDIUM      Immutability by default
Destructure parameters            MEDIUM      Cleaner function signatures
Use template literals             LOW         Over string concatenation
```

---

## 9. Project Scaffolding Templates

### 9.1 package.json (Full-Stack Next.js)

```json
{
  "name": "myapp",
  "version": "1.0.0",
  "private": true,
  "type": "module",
  "scripts": {
    "dev": "next dev --turbopack",
    "build": "next build",
    "start": "next start",
    "lint": "eslint . --max-warnings 0",
    "lint:fix": "eslint . --fix",
    "format": "prettier --write .",
    "format:check": "prettier --check .",
    "typecheck": "tsc --noEmit",
    "test": "vitest",
    "test:ci": "vitest run --coverage",
    "test:e2e": "playwright test",
    "test:e2e:ui": "playwright test --ui",
    "db:generate": "prisma generate",
    "db:migrate": "prisma migrate dev",
    "db:push": "prisma db push",
    "db:studio": "prisma studio",
    "db:seed": "tsx prisma/seed.ts",
    "clean": "rm -rf .next node_modules .turbo",
    "prepare": "husky"
  },
  "dependencies": {
    "next": "^15.0.0",
    "react": "^19.0.0",
    "react-dom": "^19.0.0",
    "@prisma/client": "^6.0.0",
    "zod": "^3.23.0",
    "zustand": "^5.0.0",
    "@tanstack/react-query": "^5.60.0",
    "class-variance-authority": "^0.7.0",
    "clsx": "^2.1.0",
    "tailwind-merge": "^2.5.0",
    "lucide-react": "^0.460.0",
    "jose": "^5.9.0"
  },
  "devDependencies": {
    "typescript": "^5.6.0",
    "@types/react": "^19.0.0",
    "@types/react-dom": "^19.0.0",
    "tailwindcss": "^4.0.0",
    "eslint": "^9.15.0",
    "prettier": "^3.4.0",
    "prettier-plugin-tailwindcss": "^0.6.0",
    "vitest": "^2.1.0",
    "@testing-library/react": "^16.0.0",
    "@testing-library/user-event": "^14.5.0",
    "@playwright/test": "^1.48.0",
    "prisma": "^6.0.0",
    "husky": "^9.1.0",
    "lint-staged": "^15.2.0"
  },
  "lint-staged": {
    "*.{ts,tsx}": ["eslint --fix", "prettier --write"],
    "*.{json,md,yml}": ["prettier --write"]
  }
}
```

### 9.2 tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES2022",
    "lib": ["DOM", "DOM.Iterable", "ES2022"],
    "module": "ESNext",
    "moduleResolution": "bundler",
    "jsx": "preserve",
    "strict": true,
    "noUncheckedIndexedAccess": true,
    "noImplicitOverride": true,
    "noFallthroughCasesInSwitch": true,
    "forceConsistentCasingInFileNames": true,
    "esModuleInterop": true,
    "resolveJsonModule": true,
    "isolatedModules": true,
    "incremental": true,
    "skipLibCheck": true,
    "noEmit": true,
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    },
    "plugins": [
      { "name": "next" }
    ]
  },
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", ".next/types/**/*.ts"],
  "exclude": ["node_modules"]
}
```

---

## 10. Troubleshooting Playbook

```
Common Issues & Resolutions
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

FRONTEND
─────────
Problem: Hydration mismatch in Next.js
  Cause:  Server & client render different HTML
  Fix:    ① Use suppressHydrationWarning for dynamic content
          ② Wrap client-only code in useEffect
          ③ Use dynamic() with { ssr: false }
          ④ Check for window/document usage in SSR

Problem: Infinite re-renders
  Cause:  Object/array in dependency array recreated each render
  Fix:    ① Memoize with useMemo/useCallback
          ② Move constant objects outside component
          ③ Use primitive values in deps
          ④ Check for missing deps in useEffect

Problem: State not updating
  Cause:  Stale closure over state value
  Fix:    ① Use functional updater: setState(prev => prev + 1)
          ② Add missing dependencies to useEffect/useCallback
          ③ Use useRef for mutable values

Problem: Layout shift (CLS)
  Cause:  Images/fonts loading without dimensions
  Fix:    ① Always set width/height on images
          ② Use font-display: swap
          ③ Reserve space with aspect-ratio
          ④ Use skeleton loading states

BACKEND
────────
Problem: N+1 query
  Cause:  Fetching related data in a loop
  Fix:    ① Use include/join in ORM queries
          ② Use DataLoader pattern for GraphQL
          ③ Batch queries with WHERE IN

Problem: Memory leak in Node.js
  Cause:  Unclosed connections, event listeners, large caches
  Fix:    ① Use connection pooling
          ② Remove event listeners in cleanup
          ③ Use WeakMap/WeakRef for caches
          ④ Monitor with --inspect flag

Problem: CORS errors
  Cause:  Misconfigured CORS middleware
  Fix:    ① Set correct origin (not '*' with credentials)
          ② Include all needed methods/headers
          ③ Handle preflight OPTIONS requests
          ④ Check browser network tab for details

Problem: Database connection exhausted
  Cause:  Too many open connections
  Fix:    ① Use connection pooling (PgBouncer, Prisma pool)
          ② Close connections in finally blocks
          ③ Set pool size based on available connections
          ④ Use serverless-optimized drivers
```

---

## 11. Technology Decision Matrix

```
┌─────────────────────┬────────────────┬───────────────┬─────────────┬──────────────┐
│ Category            │ Small Project  │ Medium Project│ Large Proj.  │ Enterprise   │
│                     │ (MVP/Startup)  │ (Growth)      │ (Scale)      │ (Corporate)  │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ Frontend Framework  │ Next.js        │ Next.js       │ Next.js      │ Next.js/     │
│                     │                │               │              │ Micro-FE     │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ State Management    │ useState +     │ Zustand +     │ Zustand +   │ Redux TK +   │
│                     │ Context        │ TanStack Q.   │ TanStack Q. │ TanStack Q.  │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ API Layer           │ Server Actions │ tRPC          │ REST + tRPC │ GraphQL +    │
│                     │ / REST         │               │             │ REST         │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ Database            │ SQLite /       │ PostgreSQL    │ PostgreSQL  │ PostgreSQL + │
│                     │ Supabase       │               │ + Redis     │ Redis + DWH  │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ ORM                 │ Prisma         │ Prisma/       │ Drizzle     │ Drizzle /    │
│                     │                │ Drizzle       │             │ Raw SQL      │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ Auth                │ NextAuth/      │ Lucia /       │ Custom JWT  │ OAuth2/      │
│                     │ Clerk          │ Custom JWT    │ + RBAC      │ SAML + IdP   │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ Hosting             │ Vercel         │ Vercel / AWS  │ AWS / GCP   │ K8s / AWS    │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ CI/CD               │ GitHub Actions │ GitHub Actions│ GH Actions +│ Jenkins /    │
│                     │                │               │ ArgoCD      │ GitLab CI    │
├─────────────────────┼────────────────┼───────────────┼─────────────┼──────────────┤
│ Monitoring          │ Vercel Analyt. │ Sentry +      │ Datadog /   │ Datadog /    │
│                     │                │ Vercel        │ Grafana     │ New Relic    │
└─────────────────────┴────────────────┴───────────────┴─────────────┴──────────────┘
```

---

## 12. Glossary

| Term | Definition |
|------|-----------|
| **SSR** | Server-Side Rendering — HTML generated on server per request |
| **SSG** | Static Site Generation — HTML generated at build time |
| **ISR** | Incremental Static Regeneration — SSG with on-demand revalidation |
| **RSC** | React Server Components — Components that run only on the server |
| **BFF** | Backend For Frontend — API layer tailored for a specific frontend |
| **ORM** | Object-Relational Mapping — Database abstraction layer |
| **RBAC** | Role-Based Access Control — Permissions based on user roles |
| **ABAC** | Attribute-Based Access Control — Permissions based on attributes |
| **CQRS** | Command Query Responsibility Segregation — Separate read/write |
| **DDD** | Domain-Driven Design — Software design around business domains |
| **CSP** | Content Security Policy — HTTP header to prevent XSS |
| **HSTS** | HTTP Strict Transport Security — Force HTTPS connections |
| **CLS** | Cumulative Layout Shift — Core Web Vital measuring visual stability |
| **LCP** | Largest Contentful Paint — Core Web Vital measuring loading |
| **INP** | Interaction to Next Paint — Core Web Vital measuring responsiveness |
| **TTL** | Time To Live — Duration before cache entry expires |
| **a11y** | Accessibility (a + 11 letters + y) |
| **i18n** | Internationalization (i + 18 letters + n) |

---

## 📎 Quick Reference Card

```
┌────────────────────────────────────────────────────────────────┐
│                    AGENT QUICK REFERENCE                       │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│  🟢 ALWAYS DO:                                                │
│    • Use TypeScript with strict mode                          │
│    • Validate inputs with Zod                                 │
│    • Handle errors explicitly                                 │
│    • Write semantic HTML                                      │
│    • Include loading & error states                           │
│    • Add aria attributes for custom components                │
│    • Use environment variables for secrets                    │
│    • Return proper HTTP status codes                          │
│                                                                │
│  🔴 NEVER DO:                                                 │
│    • Use `any` type                                           │
│    • Store secrets in code                                    │
│    • Concatenate SQL strings                                  │
│    • Trust client-side validation alone                       │
│    • Use innerHTML with user input                            │
│    • Return 200 for errors                                    │
│    • Catch errors silently (empty catch)                      │
│    • Skip authentication checks                              │
│                                                                │
│  📁 FILE NAMING:                                              │
│    Components:  PascalCase.tsx    (UserCard.tsx)               │
│    Hooks:       camelCase.ts      (useAuth.ts)                │
│    Utils:       kebab-case.ts     (format-date.ts)            │
│    Types:       PascalCase        (interface UserProfile)     │
│    Constants:   UPPER_SNAKE       (MAX_RETRY_COUNT)           │
│    Routes:      kebab-case/       (user-settings/)            │
│    Tests:       *.test.ts         (user.service.test.ts)      │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

---

> **Document Maintenance:**
> This skill document should be reviewed and updated quarterly to incorporate new framework versions, emerging patterns, and evolving best practices. All code examples should be tested against their specified runtime versions before inclusion.

---

*Built for AI agents that ship production-grade code. Every line matters.*
