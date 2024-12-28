# Tailwind CSS @apply Directive Issue with Responsive Modifiers and Pseudo-classes

This repository demonstrates a subtle bug encountered when using Tailwind CSS's `@apply` directive with responsive modifiers (`md:`, `lg:`, etc.) and pseudo-classes (`:hover`, `:focus`, etc.).

The problem occurs when applying styles via `@apply` within a responsive context. The styles fail to inherit the responsive modifier, resulting in unexpected behavior.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install Tailwind CSS.
3. Start a local web server (e.g., `python -m http.server`).
4. Open `index.html` in your browser.
5. Observe that the hover effect doesn't work as expected at the specified breakpoint.

## Solution

The solution involves restructuring the CSS to avoid using `@apply` with responsive modifiers and pseudo-classes directly. Instead, create separate classes for different responsive states and apply them as needed.

This avoids the conflicting behavior and ensures that the responsive styles are applied correctly.