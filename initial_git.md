**創建一個空的repo**
===
```
1. 在電腦上新增一個資料夾
2. 透過 cd 前往該資料夾
3. 執行 git init 指令
```
如此一來一個空的 repo 就建好了，目錄下就產生了一個 .git 目錄。<br>
其為 Git 用來跟蹤管理 repo，請勿隨意動到其中的文件，以免破壞 git repo。  <br>
  

**查看當前 git repo 的狀態**
===
### **指令 : `git status`**
```
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        initial_git.md

nothing added to commit but untracked files present (use "git add" to track)
```
可以看到 Untracked files 的檔案有 initial_git.md。
Untracked 的意思是，Git 偵測到你有新增這筆檔案，但尚未是 Git 追蹤的對象。

**加入索引**
===
#### 把檔案交給 Git ，讓 Git 開始「追蹤」目錄，此時內容加到暫存區
需要使用 `git add`，先將它加入到 staging area(索引)裡，就可以將 initial_git.md 加入到追蹤對象。

```
針對單一的檔案
$  git add <檔案名稱>
```
```
一次將所有的檔案加入索引(記得 .要空格哦！)
$ git add . 
```
以本案例來說，就必須用git add initial_git.md 來加入索引。<br>
可使用git status再次查看repo的狀態，即可查看檔案是否被成功加入索引。
```
$ git status       
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   initial_git.md
```
再次使用 git status 查看會發現此時狀態會從<font color="#008000">Untracked files</font> 變成 <font color="#008000">Changes to be committed</font> <br>

**提交版本**
===
#### 將暫存區的內容提交到儲存庫（Repository）保留
```
git commit -m "<填寫版本資訊>"
```
所以這裡我就輸入git commit -m "git basic knowledge"來提交版本後，系統如果回饋以下訊息，就恭喜你，你透過 Git 建立出第一個版本出來了。
```
$ git commit -m "git basic knowledge"
[master (root-commit) b6c3c77] git basic knowledge
 1 file changed, 35 insertions(+), 0 deletions(-)
 create mode 100644 initial_git.md
```
最後使用 `git status` 可以看到以下訊息:
```
$ git status                   
On branch master
nothing to commit, working tree clean
```
表示已將 initial_git.md 提交成一個 commit, 所以目前工作目錄上已經清空了

**查看版本**
===
```
$ git log
```
看到一個版本更新紀錄，表示你成功了！
```
commit b7443be87f8e5385d44f20baee534077b10a1fb8 (HEAD -> master)
Author: ChiaAn <32055946+Lillian0114@users.noreply.github.com>
Date:   Sat Jul 8 15:02:57 2023 +0800

    0708 git basic knowledge
```

**小結**
===
![這一小結的圖片](/git_one.png "git步驟")
```
1. 開新資料夾，git init 建立數據庫
2. 新增一個檔案
3. 加入索引：git add .
4. 提交版本：git commit -m "你要加的說明"
5. 觀看歷史紀錄：git log，並會看到一個版本紀錄
```
