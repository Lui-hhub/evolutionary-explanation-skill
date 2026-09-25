# Example: Explaining Frontend Frameworks

This example shows the intended progression for explaining frontend frameworks. It uses React as a concrete example, but the conceptual layers transfer to Vue, Angular, and similar ecosystems.

## 1. Concrete problem

A small page can be written with HTML and JavaScript. As interactions grow, several functions must update the same DOM nodes, and the displayed page can drift away from the underlying data.

## 2. Smallest workable solution

Keep an array of tasks, update it after a user action, and render the list again. This is enough for a small application.

## 3. Limitation

Adding deletion, filtering, loading states, and multiple views makes manual DOM updates hard to coordinate. The key problem becomes keeping the interface consistent with changing data.

## 4. Next concept

Introduce components. A component owns a small piece of interface logic and receives data as input. A page becomes a tree of components rather than one large script.

## 5. Further evolution

Introduce state so the framework can re-render the relevant components when data changes. Introduce routing when URLs need to select pages. Introduce a server-state tool when remote data needs loading, caching, and error handling.

## 6. Complete model

```text
user action
    -> component event
    -> local or server state update
    -> component re-render
    -> updated interface
```

The framework is useful when the coordination benefits outweigh the learning and tooling costs. A static page with little interaction may not need it.
