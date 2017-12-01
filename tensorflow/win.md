
## Dockerのインストール

Windows用のDocker設定は、[Docker for Windows のインストール](http://docs.docker.jp/windows/step_one.html#)を参考にインストール

# TensorFlowのインストールと起動

[https://hub.docker.com/r/tensorflow/tensorflow/](https://hub.docker.com/r/tensorflow/tensorflow/)

```shell
$ docker run -it -p 8888:8888 tensorflow/tensorflow
```

# Browserでの接続

```shell
http://localhost:8888/
```
