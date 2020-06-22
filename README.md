# Linux

#### Burn ISO to USB
```bash
sudo dd if=file.iso of=/dev/sdc bs=4M
```

# Git

#### Sign all commits
```bash
git filter-branch -f --commit-filter 'git commit-tree -S "$@"' HEAD
```

#### Change author on all previous commits
```bash
git filter-branch -f --env-filter \
    "GIT_AUTHOR_NAME='Your Name'; \
    GIT_AUTHOR_EMAIL='your@email.com'; \
    GIT_COMMITTER_NAME='Your Name'; \
    GIT_COMMITTER_EMAIL='your@email.com';" \
    HEAD;
```