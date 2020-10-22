# Linux

#### List all processes running
```console
foo@bar:~$ ps S
```

#### List processes for current session
```console
foo@bar:~$ jobs -l
```

#### Move process from background to foreground
```console
foo@bar:~$ fg % [job-id or job-index]
```

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

#### Create `.tar`
```console
foo@bar:~$ tar -cvf file.tar /dirname
```

#### Extract `.tar`
```console
foo@bar:~$ tar -xvf file.tar -C /output/path
```

#### Extract `.tar.gz`
```console
foo@bar:~$ tar -xzvf file.tar.gz -C /output/path
```

#### Extract `.tar.bz2`
```console
foo@bar:~$ tar -xjvf file.tar.bz2 -C /output/path
```

#### Change extension for files
```console
foo@bar:~$ find . -name *.ext1 -exec rename "s/\.ext1$/.ext2/" "{}" \;
```

### Generate RSA private key
```console
foo@bar:~$ openssl genrsa -out key.pem
```

### Generate Certificate Signing Request (CSR)
```console
foo@bar:~$ openssl req -out key.csr -key key.pem -new
```

### Generate certificate
```console
foo@bar:~$ openssl x509 -req -in key.csr -signkey key.pem -out key.crt
```

### Generate .p12 certificate
```console
foo@bar:~$ openssl pkcs12 -export -in key.crt -inkey key.pem -out cert.p12
```
