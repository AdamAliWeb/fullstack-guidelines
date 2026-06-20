# Tailwind & SASS

## References

- **[SASS Reference](https://sass-lang.com/guide/)**
- **[Tailwind Reference](https://tailwindcss.com/docs/installation/using-vite)**
- **[Prettier for Tailwind](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier)**

## Tips & Tricks

### SASS

1. Use the .scss syntax, never the original .sass syntax

2. Avoid excessive nesting in SASS to prevent specificity issues and maintain code organization.

3. Transition from @import to @use as @import is deprecated and will be removed in the future. This helps prevent global namespace pollution and reduces compilation time and output size.

### Tailwind

1.  Utilize the `@apply` rule in your **CSS** to apply **Tailwind** classes, reducing verbosity and enhancing readability.

    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

    @layer components {
      .btn-primary {
        @apply py-2 px-5 bg-violet-500 text-white font-semibold rounded-full shadow-md hover:bg-violet-700 focus:outline-none focus:ring focus:ring-violet-400 focus:ring-opacity-75;
      }
    }
    ```
