# Git
- [Learn-Git-in-30-days/README.md at master · doggy8088/Learn-Git-in-30-days · GitHub](https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/README.md)
- [Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)
- [【Git - 刪除 GitHub 上的 Repository】 - 法蘭克的iOS世界 - Medium](https://medium.com/@mikru168/github-%E5%88%AA%E9%99%A4github%E4%B8%8A%E7%9A%84%E5%B0%88%E6%A1%88-a3218b1beafe)
- [回復GIT不同區域修改 · GIT教學](https://kingofamani.gitbooks.io/git-teach/content/chapter_2/chapter_2reset_file.html)
---

# git 語法 
## 使用cmder
!!! caution
若cmder停住，":q"即可回復
!!! 

## git 使用流程

### github建立一個repo
!!! caution
github建立分支時不要加入READ.md 因為會導致無法跟本地端串接
若repo已經有檔案 則本地端需要用pull
!!!

### 建立本地file 指定為repository
```
// 移動到 tutorial 資料夾
$ cd tutorial
// 將專案資料夾建立成 git repository
$ git init
```

1. 本地(master)端 file加入追蹤
```
//追蹤 Git.md
git add "Git.md"

//加入追蹤目錄下所有檔案
//不能add 空的資料夾
//在repo裡增加新的folder要重新add repo
git add .

//解除追蹤
git rm --cached "Git.md"
```

2. 查看 git 
```
//file status
git status

//看file 修改的地方
git diff
```
3. commit file 進入 repository
```
//-m 代表commit message
git commit -m "Git.md"

//若有刪除或修改檔案 要重新add & commit進本地repo
//-a 代表 add
git commit -a -m "test.txt"
```

4. github創建repository, 本地repository(master)連接github repository(origin)
```
//登入github
git config --global user.username <你的 github 使用者名稱>

git config --global user.email "you@example.com"
git config --global user.name "Your Name"

// 本地端對應到遠端repository URL
git remote add origin <remote 網址>
```

5. push file 到 github
```
// 將本地端程式 push 到遠端檔案庫
//$ git push -u <remote name> <branch name>
//-u代表--set-upstream上游
//第一次push
git push -u origin master

//已經與github連線過，第二次以後可簡寫
git push
```

6. 刪除本地端 file
```
//直接刪除file
rm -rf <file>

//尚未add前
git rm "git.md"
```
!!! note 
若修改file副檔名，則該file要重新add

!!!

7. 刪除本地端 branch
```
//$ ls -a    #找到目录下.git
C:\Users\hmnic\Google 雲端硬碟 (b034020026@g-mail.nsysu.edu.tw)\web\jquery_tutorial (master)
λ ls -a
./  ../  .git/  panel_flip.html  README.md

//$ rm -rf  .git   #删除
C:\Users\hmnic\Google 雲端硬碟 (b034020026@g-mail.nsysu.edu.tw)\web\jquery_tutorial (master)
λ rm -rf .git

//可以看到master分支已经删除（jquery_tutorial中隐藏的.git文件夹已经删除）
C:\Users\hmnic\Google 雲端硬碟 (b034020026@g-mail.nsysu.edu.tw)\web\jquery_tutorial
λ ls
panel_flip.html  README.md
```


---
### git回復

查看commit過的版本
```
λ git log --oneline
b50e327 (HEAD -> master) HelloWorld

λ git log
commit b50e327dcf7ed990d3cdc2090d2b2cbb34ffeb0a (HEAD -> master)
Author: sfianchao1022 <sfianchao@yahoo.com.tw>
Date:   Sat Nov 30 15:52:33 2019 +0800

    HelloWorld


```

強制回到某一個版本
```
//SHA1碼的前六碼
git reset --hard b50e327
```

更新git
```
git update-git-for-windows
```

