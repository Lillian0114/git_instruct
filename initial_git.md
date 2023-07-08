**Installation**
===
```
1. 在電腦上新增一個資料夾
2. 透過 cd 前往該資料夾
3. 執行 git init 指令
```
如此一來一個空的 repo 就建好了,目錄下產生了一個 .git 目錄。
其為 Git 用來跟蹤管理 repo, 請勿隨意動到其中的文件，以免破壞 git repo。  

**查看當前 git repo 的狀態**
===
### 指令 : `git status`
```
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        initial_git.md

nothing added to commit but untracked files present (use "git add" to track)
```
可以看到 Untracked files 的檔案有 `initial_git.md`。
Untracked 的意思是，Git 偵測到你有新增這筆檔案，但尚未是 Git 追蹤的對象。

**加入索引**
===
需要使用 `git add`，先將它加入到 staging area(索引)裡，就可以將 initial_git.md 加入到追蹤對象。
```
git add <檔案名稱>
```
以本案例來說，就必須用git add initial_git.md 來加入索引。
