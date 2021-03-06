# gvim  
  
## 目的  
  
自分GVIMを即時展開できるようにする  
  
## 参照先  
  
gvimの管理ファイル置き場  
https://github.com/shinonome128/gvim  
  
Win用gvim  
https://www.kaoriya.net/software/vim/  
  
Vim8のパッケージ配置参考  
http://yoneyore.hatenablog.com/entry/2017/10/28/222955  
  
クイックラン  
https://github.com/thinca/vim-quickrun  
  
vim-fugitive  
https://github.com/tpope/vim-fugitive  
  
Glog の使い方、コミット毎のソースのリストを CW に表示  
http://vimcasts.org/episodes/fugitive-vim-exploring-the-history-of-a-git-repository/  
  
## 管理方針  
  
gvimrc, vimrc は gvim のデフォルトを使うので管理しない  
アンスコgvimrc だけカスタマイズし、Gitで管理する  
README.md に手順を書いて、Gitで管理する  
.gitignoreに管理対象外ファイル書いて、Gitで管理する  
  
## GVIMダウンロードとインスト  
  
ポータブルが良い  
  
## 管理ファイル追加  
  
GVIMインストディレクトリに移動、ローカル、VDI、試験環境によりここを変更  
```  
cd C:\Users\shino\bin\vim81-kaoriya-win64  
```  
  
Gitクローン  
```  
git clone https://github.com/shinonome128/gvim  
```  
  
設定ファイル配置と不要ディレクトリ削除  
```  
move gvim\* .  
rmdir /s /q gvim  
```  
  
## vim-quickrun追加  
  
プラグインディレクトリ作成  
```  
mkdir C:\Users\shino\bin\vim81-kaoriya-win64\vim81\pack\vim-quickrun\start  
```  
  
プラグインディレクトリに移動  
```  
cd C:\Users\shino\bin\vim81-kaoriya-win64\vim81\pack\vim-quickrun\start  
```  
  
Gitクローン  
```  
git clone https://github.com/thinca/vim-quickrun  
```  
  
## vim-fujitive追加  
  
プラグインディレクトリ作成  
```  
mkdir C:\Users\shino\bin\vim81-kaoriya-win64\vim81\pack\vim-fugitive\start  
```  
  
プラグインディレクトリに移動  
```  
cd C:\Users\shino\bin\vim81-kaoriya-win64\vim81\pack\vim-fugitive\start  
```  
  
Gitクローン  
```  
git clone https://github.com/tpope/vim-fugitive.git  
```  
  
## 管理ファイルを更新したらやること  
  
ユーザ追加  
```  
git config --local user.email shinonome128@gmail.com  
git config --local user.name "shinonome128"  
```  
  
ファイルを確認  
```  
git statu  
```  
  
ファイルが正しい場合は追加  
```  
git add 変更対象ファイル  
```  
  
対象ファイルをコミット  
```  
git commit -m "コメントを追記する"  
```  
  
GitHubに送信  
```  
git push  
```  
  
fujitive でやる場合  
```  
Gwrite  
    現在開いているソースをgit add  
Gstatus  
    新しい窓を作ってgit statusを表示  
    D で diff ショートカット  
    C で commit ショートカット  
Gdiff  
    現在のソースの変更点をvimdiffで表示  
Gcommit  
    git commit  
Gpush  
    git push  
Glog | cw  
    各コミット毎のリストを C Window に表示  
  
```  
  
以上  
