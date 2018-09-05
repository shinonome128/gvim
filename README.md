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

スキーマファイル
なんだっけ、VDI環境に移植するときにやる

クイックラン
https://github.com/thinca/vim-quickrun

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
move gvim\* .\
rmdir /s /q gvim
```

## vim-quickrun追加

プラグインディレクトリ作成
```
mkdir C:\Users\shino\Desktop\vim81-kaoriya-win64\vim81\pack\vim-quickrun\start
```

プラグインディレクトリに移動
```
cd C:\Users\shino\Desktop\vim81-kaoriya-win64\vim81\pack\vim-quickrun\start
```

Gitクローン
```
git clone https://github.com/thinca/vim-quickrun
```

## 管理ファイルを更新したらやること

ユーザ追加
```
git config --global user.email shinonome128@gmail.com
git config --global user.name "shinonome128"
```

ファイルを確認
```
git status
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

以上
