# mypkg

[![test](https://github.com/soma4649/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/soma4649/mypkg/actions/workflows/test.yml)

2023年度千葉工業大学ロボットシステム学講義内での課題提出用リポジトリです。


このリポジトリでは、talkerとlistenerという二つのノード間でROS2の通信を行います。

## このリポジトリのインストール方法
１．以下のコードを任意のディレクトリで実行してください。

```
$ git clone https://github.com/soma4649/mypkg
```
２. 以下のコードでmypkgのディレクトリに移動してください。

```
$ cd mypkg
```

## talkerとlistenerについて

### talker

0.5秒おきに０から１ずつ数を足していき、結果をメッセージとしてlistenerに送る。この時、メッセージはcountupというトピックを通じて送られる。

### listener

talkerから受け取ったメッセージを端末に出力する。

## launchファイルについて

talkerとlistenerを両方同時に実行する。

### 使用方法
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/takeru/.ros/log/2023-12-28-14-51-06-028442-LAPTOP-E07E4SPD-2096
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [2098]
[INFO] [listener-2]: process started with pid [2100]
[listener-2] [INFO] [1703742666.844018173] [listener]: Listen: 0
[listener-2] [INFO] [1703742667.337759341] [listener]: Listen: 1
[listener-2] [INFO] [1703742667.845937005] [listener]: Listen: 2
[listener-2] [INFO] [1703742668.337141779] [listener]: Listen: 3
[listener-2] [INFO] [1703742668.840204467] [listener]: Listen: 4
[listener-2] [INFO] [1703742669.337235977] [listener]: Listen: 5
```

## 動作確認済みの環境
### ソフトウェア
・python3.7~3.10

### テスト環境
・Ubuntu 20.04.6 LTS on Windows

## 著作権
* このソフトウェアパッケージは、３条項BSDライセンスの下、再頒布および使用が許可されています.
* このパッケージのコードは、下記のスライド( CC-BY-SA 4.0 by Ryuichi Ueda)のものを、本人の許可を得て自身の著作物としたものです.
   * ryuichiueda/my_slides/robosys_2022[[Github Pages](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)]
* ©　2023 Takeru Soma
