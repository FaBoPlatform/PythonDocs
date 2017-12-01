## Dockerのインストール

[Docker公式サイト](https://www.docker.com/) で Get Started を選択、次にDownload Docker for Macを選択し本体をダウンロードします。ダウンロード終了後インストールを行い、終了後に表示されるアイコンをクリックすることでDockerが起動します。

![](/img/docker001.png)

![](/img/docker002.png)

![](/img/docker003.png)

# TensorFlowのインストールと起動

[https://hub.docker.com/r/tensorflow/tensorflow/](https://hub.docker.com/r/tensorflow/tensorflow/)

```shell
$ docker run -it -p 8888:8888 tensorflow/tensorflow
```

# Browserでの接続

```shell
http://localhost:8888/
```
