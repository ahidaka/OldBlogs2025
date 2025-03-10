# 2024-0922.md

## セミナー準備とYocto

今回の内容

IoT システム開発における WSL
　（ハンズオンセミナー紹介）
Yocto ディスク容量考察
エクスポートとインポート
WSL の ネットワークアプリ
WSL と 組み込みシステム

口上

本セミナでは，以前のインターフェース掲載記事を元した単純な入門用ドライバと，オリジナルの汎用IoTドライバを教材に，組み込みLinuxにおけるドライバ開発の基本，最近のAI利用のコーディングから，デバッグ手法とパッケージングまでを習得することを目指します．開発環境はPC 1台で開発の全てをホストする，WindowsとWSLを使用します．合わせて，その上でYocto Projectを稼働させて開発するためのノウハウも伝授します


経緯・いきさつ

CQ出版 編集部から依頼
AVNET のボードでハンズオンセミナー
基板はi.MX 8ULP で開発環境は Yocto Project
テーマはLinuxドライバー開発、1日

Yocto ディスク容量考察

i.MX 8ULP 用の場合
Ubuntu 20.04 使用容量：290GB
SDK含めたシステム構築に 2～6時間
　　↓
WSLで実験：
仮想ディスク容量：96.9GB
さらにzip 圧縮：37.1GB

## 考察




エクスポートとインポート

エクスポート

WSL停止後、仮想ディスクを外部出力
一般形式： wsl --export Distribution “Export file path"

例：wsl --export Ubuntu-20.04 "D:\WSL\vdisk.tar"

インポート

WSL停止後、仮想ディスクを指定して登録
一般形式： wsl --import New dist-name "Import file path"

例：wsl --import Ubuntu-20.04cq "D:\WSL\vdisk.tar"



WSLのネットワークアプリ

注意点：WSL ネットワーク

図


WSL と組み込みシステム

Windows 開発ツールが便利
複数ユーザー、複数 Distribution 使い分け
Yocto Project が安定動作
Yocto Project がより使い易くなる(vs. Docker, VM, …)
エクスポートとインポート
USB とシリアルポート も使える








Yoctoが厄介そうなので何回も動作検証した
（外部接続：結局は使わなかった）

試したことなど。

沢山試行錯誤した。

Import/Export 容量

これがうまくいった


セミナーの準備

## 今回の発表内容


関連リンク

YouTube


