# **File Maintenace Commands**

---

- cp
- rm
- mv
- mkdir
- rmdir or rm- r
- chgrp
- chown

---

### cp

```sh
cp data data1   # cp data as data1
cp data /temp   # cp data to temp dir as data
```

### rm

```sh
rm data # remove data from current dir
```

### mv

```sh
mv data data1   # rename data to data1 in same dir
mv puddy /tmp   # move puddy to /tmp dir
```

### mkdir

```sh
mkdir data  # make a dir with name data
```

### rmdir or rm -r

```sh
rmdir data  # remove dir data
rm -r data  # remove dir    ::  rm -rf = forcefully remove sub-dirs and its contents :: Recursively
```

### chgrp

```sh
chgrp root file    # ownership of file group to root
```

- root access needed

### chown

```sh
chown root file1    # ownership to root of file1
chown imrul:imrul file1 # ownership and group to imrul of file1
```

