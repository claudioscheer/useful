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

#### Create branch from commit
```console
foo@bar:~$ git checkout -b branch-name <sha1-of-commit>
```