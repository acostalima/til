# Show hidden files in Finder

* Make it persistent for the current session and between restarts:

```
$ defaults write com.apple.Finder AppleShowAllFiles YES
$ killall Finder
```

* Toggle manually using the shortcut ⌘ + ⇧ + . (period)
