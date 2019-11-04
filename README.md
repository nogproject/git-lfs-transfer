# Git LFS Transfer
By spr
<!--@@VERSIONINC@@-->

## Introduction

Git LFS Transfer contains helper programs to transfer LFS content without HTTP.

`git-lfs-standalonetransfer-ssh` requires at least Git LFS 2.3.1.  Support for
Git LFS before 2.3.1 has been removed 2017-11-09.  See Git history for details.

`git-lfs-standalonetransfer-file` should be used with Git LFS 2.4.1 or later.

Install:

```sh
cd git-lfs-transfer
pip3 install -r requirements.txt

ls -l "$(pwd)"/bin/git-lfs-standalonetransfer-*
ln -s "$(pwd)"/bin/git-lfs-standalonetransfer-* ~/bin

git-lfs-standalonetransfer-ssh -h
git-lfs-standalonetransfer-file -h
```

See `git-lfs-standalonetransfer-ssh -h` for details how to configure a repo to
use Git LFS SSH Transfer.  In brief, run:

```sh
git config lfs.customtransfer.ssh.path git-lfs-standalonetransfer-ssh
git config lfs.https://vishost//vis/data/.standalonetransferagent ssh
```

See `git-lfs-standalonetransfer-file -h` for details how to configure Git LFS
for local repos.  In brief, run:

```sh
git config --global lfs.customtransfer.file.path git-lfs-standalonetransfer-file
git config --global lfs.file:///.standalonetransferagent file
```

Use Git LFS as usual.
