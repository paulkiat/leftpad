# LeftPad

A hyper-opinionated, full-stack JavaScript framework simplifying web development.

## Introduction to LeftPad

LeftPad is a hyper-opinionated, full-stack JavaScript framework designed to simplify the journey from learning basic web development—HTML, CSS, and JavaScript—to building robust full-stack applications. It aims to reduce the complexity and fragility often associated with shipping applications using JavaScript by offering a stable and easy-to-maintain architecture.

## Core Principles

### Be Hyper-Opinionated

LeftPad is tailored for single-page applications and embraces a specific approach that may not suit everyone, and that's okay.

### Learn from Experience

* Routes are defined on the server where they belong.
* Skepticism towards new technologies until proven effective; practical demos are valued over theoretical discussions.

### Limit Third-Party Dependencies

* Prefers a DIY approach when possible.
* Aims to reduce dependencies to zero over time by implementing functionality in-house.

### Keep APIs Backwards Compatible

* Ensures that any changes between versions are either fixes or new features.
* Commits to preventing breaking changes, striving for a single major version with subsequent minor or patch updates.

## Framework Components

LeftPad consists of four main packages:

### LeftPad.js/ui

A front-end framework for building UI components using standard HTML, CSS, and JavaScript.

#### Key Features:

**No New Syntax:**
* Components are built without introducing new languages or syntaxes.
* Component Structure: Components include a `render()` function that returns HTML strings using JavaScript template literals.

**Utility Functions:**
* `component()`: Renders another component for composition.
* `each()`: Iterates over arrays to render data.
* `i18n()`: Handles internationalization strings.
* `when()`: Conditionally renders HTML based on variables.

**Additional Options:**
* `css`: Defines component-specific styles.
* `events`: JavaScript DOM events scoped to the component.
* `methods`: Domain-specific functions accessible via the component instance.
* `lifecycle`: Methods like `onBeforeMount`, `onMount`, `onBeforeUnmount` for component lifecycle management.
* `state`: Manages component state, modifiable via `.setState()`.

**HTTP Requests:**
* `get()`: Performs HTTP GET requests with input validation and selective fetching.
* `set()`: Performs HTTP POST requests with similar capabilities.

**User Accounts:**
* Provides an `accounts` object with methods: `signup()`, `login()`, `logout()`, `recoverPassword()`, and `resetPassword()`.

### LeftPad.js/server

A back-end framework built on Node.js and Express.js.

#### Key Features:

**Application Initialization (`node.app()`):**
* Registers routes with organized syntax and a custom `res.render()` function for rendering components.
* Registers APIs using getter and setter functions.
* Allows custom middleware and event listeners for `uncaughtException` or `unhandledRejection`.

**Server-Side Rendering (`res.render()`):**
* Performs server-side rendering of components as static HTML and CSS.
* Embeds compiled JavaScript for client-side hydration.
* Utilizes automatic scripts for mounting and hydrating components on the client.

### LeftPad.js/test

A testing library for writing and instrumenting tests on both the front-end and back-end of your LeftPad application.

### LeftPad.js/cli

A command-line tool for:
* Creating new LeftPad applications.
* Running development servers.
* Deploying applications via PK's Elastic service.

## Philosophy and Commitment

### Long-Term Stability
LeftPad is committed to ensuring that components built today will work a decade later without modification.

### Developer Experience
Aims to provide a balance between rapid early development and long-term maintainability through sound architectural decisions.

### Minimal Magic
Apart from the `res.render()` function, LeftPad avoids hidden complexities, promoting transparency and simplicity.

## Conclusion

LeftPad is designed for developers who value stability, simplicity, and a pragmatic approach to building full-stack JavaScript applications. By focusing on core web technologies and minimizing dependencies, it provides a robust platform that evolves gracefully over time without disrupting existing codebases.
