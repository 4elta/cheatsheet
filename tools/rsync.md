# rsync

## download all files from a publicly accessible rsync daemon

* archive mode (`a`)
* keep partially transferred files and show progess during transfer (`P`)

```
rsync -aP rsync://<host>:</path/to/dir> <path/to/dir>
```

## [...](https://download.samba.org/pub/rsync/rsync.1)
