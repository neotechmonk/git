### Create new file - `original.txt`
``` shell
ehco "Original File" > original.txt
```

### Create a copy of the original - `modified.txt`
``` shell
cp original.txt modified.txt
```

### Add changes to `modified.txt`
``` shell
ehco "New line " >> modified.txt
```

### See changes in `modified.txt`
```shell
# -u flag is to provide contxt of the diff
diff -u original.txt modified.txt
```

### save changes in `change.diff` file
```shell
diff -u original.txt modified.txt > change.diff
```

### Merge changes from  `change.diff` file
```shell
patch original.txt change.diff
```