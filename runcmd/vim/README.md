# VIM

## Vundle

vimのプラグインを管理するパッケージ

```shell
cd ~/.vim/bundle/
git clone https://github.com/VundleVim/Vundle.vim.git
```

他には

- https://github.com/Shougo/dein.vim

各プラグインは

```shell
~/.vim/bundle
```
下に置いておく。

```shell
vim +PluginInstall +qall
```

でプラグインすべてをインストールすることができる。


## vim indent 

```shell
cd ~/.vim/bundle
git clone git://github.com/nathanaelkane/vim-indent-guides.git
```


## IMEのON/OFFを切り替える

インサートモード中に日本語で文章を入力していて、ESCでノーマルモードに戻っても日本語入力の状態のままなので
vimのコマンドがすぐに打てない。


### ESCでIMEのON/OFFの切り替え

ことえりにはその機能はないので、Google日本語入力を使用する。
