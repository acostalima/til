# Compress without \_\_MACOSX and .DS\_Store files

* Exclude the specified files at compress time:

```
$ zip -r file.zip -x "__MACOSX" -x "*.DS_Store"
```

* Remove the specified files from an existing compressed file:

```
$ zip -d file.zip "__MACOSX/*" "*.DS_Store"
```
