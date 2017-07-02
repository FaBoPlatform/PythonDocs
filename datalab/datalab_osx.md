# Google Cloud DataLab

Google Cloud DataLabは、データを探索、視覚化、分析、変換するための、生産性の高いインタラクティブな統合ツールです。Google Cloud Datalabは、Dockerで起動、GCPのインスタンスで起動が可能である。今回は、ローカル環境でDockerで起動していく。


## Dockerのインストール

[Docker公式サイト](https://www.docker.com/) で Get Started を選択、次にDownload Docker for Macを選択し本体をダウンロードします。ダウンロード終了後インストールを行い、終了後に表示されるアイコンをクリックすることでDockerが起動します。

![](/img/docker001.png)

![](/img/docker002.png)

![](/img/docker003.png)


## Datalab用 Docker Imageの起動

[OS Xで実行:プロジェクトIDを未指定]
```shell
$ cd ~
$ mkdir -p ./datalab
$ docker run -it -p 127.0.0.1:8081:8080 -p 6006:6006 -v "${HOME}/datalab:/content" \
gcr.io/cloud-datalab/datalab:local
```
|引数|意味|
|:--|:--|
|-p 127.0.0.1:8081:8080 | Datalabに8081ポートでアクセスできるようにする|
|-p 6006:6006|TensorBoardに6006ポートでアクセスできるようにする|
|-v "${HOME}/datalab:/content"|OSX上の${HOME}/datalabフォルダとDocker内の/contantを連携する|
|gcr.io/cloud-datalab/datalab:local|起動するDocker Image|

Browserで、localhost:8081に接続します。

![](/img/datalab001.png)

{%youtube%}ThdjMFOPDkw{%endyoutube%}

```
print "Hello World"
```

{%youtube%}ZIcjCXPyAUI{%endyoutube%}

