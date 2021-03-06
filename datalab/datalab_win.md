# Google Cloud DataLab

Google Cloud DataLabは、データを探索、視覚化、分析、変換するための、生産性の高いインタラクティブな統合ツールです。Google Cloud Datalabは、Dockerで起動、GCPのインスタンスで起動が可能である。今回は、ローカル環境でDockerで起動していく。

## Cloud SDKを経由してGCPのプロジェクトと連携

Datalabは、Cloud SDKを経由して、GCPのプロジェクトと連携が可能になる。もちろん、連携しないで起動する事も可能である。GCPの設定時に、プロジェクトを作成した場合は、そのプロジェクトと連携できるので、GCPのプロジェクトIDを、Cloud Shellを起動し、コマンドで取得する。

[CloudMLで実行]
```shell
$ gcloud projects list
```

## Dockerのインストール

[Docker for Windows のインストール](http://docs.docker.jp/windows/step_one.html#)を参考にDocker for Windowsをインストールする。

## Datalabの起動

[プロジェクトIDを指定]
```shell
$ cd ~
$ mkdir -p ./datalab
$ docker run -it -p 127.0.0.1:8081:8080 -p 6006:6006 -v "${HOME}/datalab:/content" \
 -e "PROJECT_ID=プロジェクトID"  \
gcr.io/cloud-datalab/datalab:local
```

[プロジェクトIDを未指定]
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

## Datalabにアクセス

Browserで、localhost:8081に接続します。

![](/img/datalab001.png)

## Hello World

![](/img/datalab002.png)

![](/img/datalab003.png)

![](/img/datalab004.png)

![](/img/datalab005.png)

![](/img/datalab006.png)

```python
import matplotlib.pyplot as plt
import numpy as np
%matplotlib inline

x = np.arange(0, 10, 0.1)
y = np.sin(x)

plt.plot(x,y)
plt.show()
```
