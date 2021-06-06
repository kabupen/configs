# Docker for mac

## Install

- https://hub.docker.com/editions/community/docker-ce-desktop-mac
  - どのCPUが搭載されているかで、インストールすべきパッケージが異なる

- インストール後、アプリケーションからdockerを起動すると使用できるようになる


## How to use

```shell
docker images # pullしているイメージの確認
```

## Tensorflow

作成済みイメージをdockerhubから持ってくる

```shell
docker pull tensorflow/tensorflow:1.15.5-gpu-py3
```

コンテナ内のbashを起動して作業する

```shell
docker run -it docker.io/tensorflow/tensorflow:1.15.5-gpu-py3 /bin/bash
```

このままだと
> WARNING: You are running this container as root, which can cause new files in
mounted volumes to be created as the root user on your host machine.

というワーニングが出るので、避けるには、

```shell
docker run -u $(id -u):$(id -g) -it docker.io/tensorflow/tensorflow:1.15.5-gpu-py3 /bin/bash
```

とオプションを追加する。

ホストOSのディレクトリをコンテナにマウントするには

```shell
-v /Users/xxx/workspace/:/Users/xxx/workspace/
```

のオプションを付けることでコンテナから見ることができる。
コンテナ内で作成したファイルは、コンテナから出てもホストOSから見ることもできる。
