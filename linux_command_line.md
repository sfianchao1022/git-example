# linux 基本指令
[Linux Command 命令列指令與基本操作入門教學](https://blog.techbridge.cc/2017/12/23/linux-commnd-line-tutorial/)

切換至根目錄: cd / 

切換至上一層目錄: cd .. 

切換至目前目錄下的相對目錄: cd ./目錄名 

切換至所指定絕對路徑的目錄: cd 磁碟名:/目錄名 

切換至指定磁碟: cd 磁碟名: 

!!! caution
若遇到空格或特殊符號，前面要加入"\"
```
(base) zhaoshoufeng@zhaoshoufengdeMacBook-Pro git-example % ls
README.md		git_tutorial.md		linux command line.md	markdown_tutorial.md	test.txt
(base) zhaoshoufeng@zhaoshoufengdeMacBook-Pro git-example % rm -rf linux\ command\ line.md
(base) zhaoshoufeng@zhaoshoufengdeMacBook-Pro git-example % ls
README.md		git_tutorial.md		markdown_tutorial.md	test.txt
```
!!!

# mac terminal 指令
[Mac OS X Terminal 終端機常用語法教學 \| 梅問題．教學網](https://www.minwt.com/mac/14653.html)

***

## linux 目錄配置

Linux 目錄樹配置標準參考：FHS (Filesystem Hierarchy Standard)  
FHS 標準，主要定義三段目錄：  
最上層根目錄 /  
次層 /usr 及  
次層 /var 的目錄內容。 

各目錄大致內容：

/ 根目錄

/etc, /bin, /dev, /lib, /sbin 這五個次目錄

都要與根目錄一起，不可為獨立的 partition。

/bin 放常用執行檔如：ls, mv, rm。

/boot 放 Linux 核心及開機相關檔案。

/grub 放 grub 開機管理程式。

/dev 放裝置有關的檔案，Linux 把裝置當成檔案看待。

/etc 放系統在開機過程需要讀取的檔案。

/rc.d 記錄開關機過程中的 scripts 檔案。

/init.d 放所有服務預設的啟動 scripts。

/xinetd.d 放一些額外的服務。

/X11 放 X window 有關的設定檔。

/home 使用者的家目錄。

/lib 放 Linux 執行或編譯程式時要使用的函式庫 (library)。

/mnt 軟碟及光碟預設掛載的地方。

/proc 虛擬檔案系統，不佔任何硬碟空間，

放置的資料在記憶體中。放系統核心與執行程序的資訊。

/root 系統管理員的家目錄。

/sbin 放系統管理常用的程式如：fdisk, mount。

/tmp 一般使用者暫時存放檔案的地方。

/usr 此目錄包括許多子目錄，用來存放系統指令、

安裝程式及套件。

/bin 放使用者可執行的程式執行檔。

/include 放一些套件的 header 檔。

/lib 內含許多程式與子程式所需的函式庫。

/local 升級或額外安裝的程式擺放的目錄，

以區分原始系統安裝的程式。

/man 放程式的說明檔。

/sbin 放系統管理員可用之程式。

/src 放核心原始碼。

/share 放安裝的程式及套件。

/doc 放系統說明文件。

/man 放程式說明檔。

/X11R6 X window system 存放相關的目錄。

/var 放系統執行中，常態性變動的檔案。

/cache 程式執行中的暫存檔。

/lib 程式執行中需要使用的資料檔案，例如 rpm 資料庫系統。

/log 登錄檔。

/run 某些程式或服務啟動後會將其 PID 放置於此。

/spool 放一些佇列資料。

例如主機收到電子郵件後，放於 /var/spool/mail。


