# Jupyter-noterbookの設定

## vim キーバインド

- https://github.com/lambdalisue/jupyter-vim-binding

```shell
mkdir -p $(jupyter --data-dir)/nbextensions
cd $(jupyter --data-dir)/nbextensions
git clone https://github.com/lambdalisue/jupyter-vim-binding vim_binding
jupyter nbextension enable vim_binding/vim_binding
```

これで使用できるようになっている。

# JupyterLab
## vim keybind

```shell
jupyter labextension install @jupyterlab/toc
```
