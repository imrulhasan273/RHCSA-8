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

---

# **Soft and Hard Links**

---

- `inode` : pointer or number of a file on the hard disk
    - Computer doesn't recognize the file name.
    - Computer knows a file with `inode`.

- `soft link` : Linked will be removed if file is removed or renamed.

- `hard link` : Deleting , renaming or moving the original file will not affect the hard link.

### Hard and Soft Link

```sh
ln      # Hard Link
ln -s   # Soft Link
```

![](i/1.png)

---

### Soft Link

```sh
ls -ltri  # to see inode of files
# 40813871623084217 -rw-r--r-- 1 imrul imrul 12 Aug 20 14:37 hulk
```

```sh
/home/imrul $ touch hulk
/home/imrul $ ls -ltri      # inode : 40813871623084217
/home/imrul $ cd /tmp
/tmp $
/tmp $ ln -s /home/imrul/hulk   # Soft Link Created
/tmp $ ls -ltri             # inode : 52635820644932163
# so hulk in imrul and linked hulk in tmp has different inode.
```

### Hard Link

```sh
/home/imrul $ touch hulk
/home/imrul $ ls -ltri      # inode : 156500087051133528
/home/imrul $ cd /tmp
/tmp $
/tmp $ ln /home/imrul/hulk   # Hard Link Created
/tmp $ ls -ltri             # inode : 156500087051133528
# so hulk in imrul and linked hulk in tmp has same inode.
```

---

# **Input and Output Redirects**

---


