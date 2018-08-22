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

## 管理方針

gvimrc, vimrc は gvim のデフォルトを使う
_gvimrc をカスタマイズする

## 更新変更作業

GVIMインストディレクトリに移動、ローカル、VDI、試験環境によりここを変更
```
cd C:\Users\shino\bin\vim81-kaoriya-win64
```

Gitクローン
```
git clone https://github.com/shinonome128/gvim
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

以上
