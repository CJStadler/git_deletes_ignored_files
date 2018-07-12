# Git Deletes Ignored File Demonstration
Testing whether git will delete an ignored file if you checkout a commit
where it was tracked and then return to a commit where it is ignored.

## Steps
```
$ touch untracked_file
$ ls
README.md untracked_file
$ git checkout 068c1c
HEAD is now at 068c1c0... Initial commit
$ ls
README.md untracked_file
$ cat untracked_file
This is the original tracked version.
$ git checkout master
Previous HEAD position was 068c1c0... Initial commit
Switched to branch 'master'
$ ls
README.md
```
