# Git - notes
## 目錄

* 安裝
* 設定
* 目前用到的指令
* 設定不需要放在git上的檔案
* 查看檔案中某行是誰更變的
* 救回被刪除的檔案
* 分支

### 安裝
``` sh 
sudo apt-get install git
```
### 設定
``` sh 
git config --global user.name 'username'
git config --global user.email 'username@wefwe'
#確認config
git config --list
#自定義指令
git config --global alias.自定義指令 '指令'
```
### 目前用到的指令
``` sh
git status
git clone 'url.git'
#export GIT_SSL_NO_VERIFY=1  顯示CRLfile: none 就添加環境變數
git add filename or git add .
--git add -p filename 選擇e 可編輯上傳至暫存區的內容
git commit -m 'notes'
git push
git pull
```
### 設定不需要放在git上的檔案
``` sh
vim .gitignore
/filename
#只會限制未推上git的檔案

git update-index --assume-unchanged filename
#如果要限制已推上的檔案 直接打指令
git update-index --no-assume-unchanged filename
#解除限制
git ls-files -v
#顯示限制名單
```
### 查看檔案中某行是誰更變的
``` sh
git blame filename
#須在該目錄下 , 可代參數例如：git blame -L 1,3 filename
```
### 救回被刪除的檔案
``` sh
git checkout filename
#可代參數例如：git checkout HEAD~2 filename 可以理解成 git checkout filename 並git add filename & git commit
git reset HEAD~2
#返回到前2次的版本,查看版本git log --oneline
git reset 版本號碼 --mixed/soft/hard
#查看返回紀錄 git reflog or git log -g
```
### 分支
``` sh
git branch
#列出分支
git checkout -b cat
#建立並前往分支
git merge cat
#合併 cat分支到目前的分支

```

### 使用token push
![](https://i.imgur.com/agpJP0H.png)
![](https://i.imgur.com/gz5XY0u.png)
![](https://i.imgur.com/59FMgY7.png)
![](https://i.imgur.com/Wyv9q7I.png)
![](https://i.imgur.com/HmAfaJ0.png)
![](https://i.imgur.com/ASfgyUK.png)
![](https://i.imgur.com/s4Iltnl.png)
![](https://i.imgur.com/3a5xPSp.png)

