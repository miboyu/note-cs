# 永久删除git仓库中的文件

> https://blog.csdn.net/u010295496/article/details/72862671

``` bash
# Remove files (FILES_TO_BE_REMOVED)
$ git filter-branch --force --index-filter \
> 'git rm --cached --ignore-unmatch FILES_TO_BE_REMOVED' \
> --prune-empty --tag-name-filter cat -- --all

# Reclaim space
$ rm -rf .git/refs/original/
$ git reflog expire --expire=now --all
$ git gc --prune=now
$ git gc --aggressive --prune=now

# Push to remote
$ git push origin --force --all
```
