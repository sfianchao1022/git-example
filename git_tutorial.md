# Git
[Learn-Git-in-30-days/README.md at master · doggy8088/Learn-Git-in-30-days · GitHub](https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/README.md)
[Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)
# git 語法
## 使用cmder

### git 使用流程 

```
// 移動到 tutorial 資料夾
$ cd tutorial
// 將專案資料夾建立成 git repository
$ git init
```

1. 本地(master)端 file加入追蹤
```
git add "Git.md"

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


