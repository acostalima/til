# List top-level packages installed with Brew

* List installed formulae that are not dependencies of another installed formula alongside their description:

```
$ brew leaves --installed-on-request | xargs -n1 brew desc
```

* List the dependency tree of installed formulae that are not dependencies of another installed formula:

```
$ brew deps --tree $(brew leaves --installed-on-request)
```

:warning: `brew leaves` does not output packages installed with Cask.
