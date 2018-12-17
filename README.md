# Git - notes
## 目錄

* 安裝
* 設定
* 目前用到的指令
* 設定不需要放在git上的檔案
* 查看檔案中某行是誰更變的
* 救回被刪除的檔案
* splash

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
git add filename
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
```
### 
