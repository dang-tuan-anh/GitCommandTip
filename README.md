# Checkout a specific directory
## Method 1 (inline command)
```
git init
git remote add orgin https://github.com/dang-tuan-anh/GitCommandTip
git fetch
git checkout origin/master -- GitCommand/subdirectory
```
## Method 2 (change config)
1. Step 1
```
git init
git remote add orgin https://github.com/dang-tuan-anh/GitCommandTip
git config core.sparseCheckout true
```
2. Step 2: create file .git/info/sparse-checkout with content of specific directories
```
/SpecificDirectory1
/SpecificDirectory2
!/SpecificDirectory3 -> this directory will not be checkout
```
3. Step 3
```
git pull origin master
```
# Reference
https://help.github.com/categories/managing-remotes/
