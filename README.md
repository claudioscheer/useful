# Linux

#### Burn ISO to USB
```console
foo@bar:~$ sudo dd if=file.iso of=/dev/sdc bs=4M
```

# Git

#### Sign all commits
```console
foo@bar:~$ git filter-branch -f --commit-filter 'git commit-tree -S "$@"' HEAD
```

#### Change author on all previous commits
```console
foo@bar:~$ git filter-branch -f --env-filter \
    "GIT_AUTHOR_NAME='Your Name'; \
    GIT_AUTHOR_EMAIL='your@email.com'; \
    GIT_COMMITTER_NAME='Your Name'; \
    GIT_COMMITTER_EMAIL='your@email.com';" \
    HEAD
```

# Bash

#### For with index
```bash
n=3
for ((i = 0; i < $n; i++)); do
    echo $i
done
```

#### For in list
```bash
list=(0 1 2)
for i in "${list[@]}"; do
    echo $i
done
```