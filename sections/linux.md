# Linux

#### Burn ISO to USB
```console
foo@bar:~$ sudo dd if=file.iso of=/dev/sdc bs=4M
```

#### Get largest directories
```console
foo@bar:~$ du -ah . | sort -rh | head -n 10
```

#### Get largest files
```console
foo@bar:~$ find . -type f -exec du -Sh {} + | sort -rh | head -n 10
```

#### Get files changed between two dates
```console
foo@bar:~$ find . -type f -newermt 2020-07-01 ! -newermt 2020-07-02
```

```console
foo@bar:~$ find . -type f -newermt "2020-07-01 00:00:00" ! -newermt "2020-07-02 00:00:00"
```

#### Get files from 15 minutes ago until now
```console
foo@bar:~$ find . -type f -mmin -15
```