# git-work-dir

Change refs to lfs in symbol links to improve usability for both work directories isolation and Git LFS support.

## Usage

```
./git-new-workdir <repository> <new_workdir> [<branch>]
```

## Introduction

`refs` directory contains all branch status. If shared same one, different repository will be interference each other after fetch or pull. The local branch will be updated with remote tracking branch.

`lfs` directory is using for Git LFS. There are too many big files in the directory. So it should be share with all work directories.

## Changes

1. `refs` to `lfs` in line 82.
2. Copy `refs` from source git repository to new repository.
