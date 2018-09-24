# git-work-dir

Change refs to lfs in symbol links to improve usability for both work directories isolation and Git LFS support.

## Introduction

`refs` directory contains all branch status. If shared same one, different repository will be interference each other after fetch or pull. The local branch will be updated with remote tracking branch.

`lfs` directory is using for Git LFS. There are too many big files in the directory. So it should be share with all work directories.

## Changes

Only one change: `refs` to `lfs` in line 82.
