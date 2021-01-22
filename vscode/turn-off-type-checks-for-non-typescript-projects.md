# Turn off validation for non-TypeScript projects

When working on Flow or JS codebases, TS can get in your way by signalling irrelevant errors. To avoid this, disable the following settings in your project:

```javascript
{
  "javascript.validate.enable": false,
  "typescript.format.enable": false,
  "typescript.validate.enable": false,
}
```

You can do so by creating a `.vscode/settings.json` file in the project's root directory.

Note that `javascript.*` setting applies to JavaScript files only and `typescript.*` ones apply to TypeScript only. This means you can get validation errors even if you just disable TypeScript.

> Source: [https://stackoverflow.com/a/51993691/1694191](https://stackoverflow.com/a/51993691/1694191)

