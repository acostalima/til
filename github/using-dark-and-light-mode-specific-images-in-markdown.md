# Using dark and light mode-specific images in markdown

a. Append fragment to image URL:

```markdown
![dark](https://til.andrecostalima.pt/dark.png#gh-dark-mode-only)
![light](https://til.andrecostalima.pt/light.png#gh-light-mode-only)
```

b. Use `<picture>` HTML element combined with `prefers-color-scheme` media query:

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://til.andrecostalima.pt/dark.png">
  <img src="https://til.andrecostalima.pt/light.png">
</picture>htm
```
