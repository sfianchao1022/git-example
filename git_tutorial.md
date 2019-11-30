# Git
[Learn-Git-in-30-days/README.md at master · doggy8088/Learn-Git-in-30-days · GitHub](https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/README.md)
[Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)
[【Git - 刪除 GitHub 上的 Repository】 - 法蘭克的iOS世界 - Medium](https://medium.com/@mikru168/github-%E5%88%AA%E9%99%A4github%E4%B8%8A%E7%9A%84%E5%B0%88%E6%A1%88-a3218b1beafe)
[回復GIT不同區域修改 · GIT教學](https://kingofamani.gitbooks.io/git-teach/content/chapter_2/chapter_2reset_file.html)
---

# git 語法
## 使用cmder

### git 使用流程 

建立本地file 指定為repository
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
```

4. github創建repository, 本地repository(master)連接github repository(origin)
```
//登入github
git config --global user.username <你的 github 使用者名稱>

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

//第二次以後可簡寫
git push
```

6. 刪除本地端 file
```
git rm "git.md"
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



