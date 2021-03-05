## 【D+IO Product #5】XModalAirConditionerSpeaker<br>
### 〜 既存のエアコンにクロスモーダル機能をアドオンできる D+IO Product 〜

<img width="500px" src="https://panasonic.co.jp/design/flf/assets/img/works/doing_io/doing_io_xmodal_aircon_speaker.jpg">


既存のエアコンにクロスモーダル機能をアドオンできる「クロスモーダルエアコンスピーカー」の作り方を紹介します。

このクロスモーダルエアコンスピーカーをご家庭のエアコンに取り付けることで、リモコンの赤外線操作信号を読み取り、
冷房なら涼しく感じる音、暖房なら暖かく感じる音をスピーカーから出力し、体感温度のさらなる上げ下げ効果を期待することができます。

### プロダクト概要

自宅で過ごす時間が長くなったことで家庭での消費電力が増加しているそうです。

中には毎月の電気料金が高く、気にかけている人も多いのではないでしょうか。

しかし、暑い夏や寒い冬を家で快適に過ごすために、ついつい設定温度を強めに設定してしまいがちです。

<br>

そこで、人間が持つ様々な感覚を"だます"ことで体感温度をコントロールし、設定温度を少しでも緩めることができないかと考えました。

「クロスモーダル」という方法です。

<br>

例えば、日本人は風鈴の音を聞くと、脳が涼しいイメージをして、体感温度を下げる効果があると言われています。

このクロスモーダルエアコンスピーカーでは、ご家庭のエアコンに取り付けることで、リモコンの赤外線操作信号を読み取り、 冷房なら涼しく感じる音、暖房なら暖かく感じる音をスピーカーから出力し、体感温度のさらなる上げ下げ効果を期待することができます。

<br>

さらには設定温度を緩め、消費電力を抑えることができるかもしれません。

<br><br>

**ソースコードは別リポジトリです**
<br>[https://github.com/panasonic-corporation/doingio-xmodal-aircon-speaker](https://github.com/panasonic-corporation/doingio-xmodal-aircon-speaker)

<br><hr>

##  D+IO Project

**パナソニック株式会社/FUTURE LIFE FACTORY**

[D+IO プロジェクト詳細](https://panasonic.co.jp/design/flf/works/doing_io/)

<a href="https://panasonic.co.jp/design/flf/works/doing_io/"><img width="500px" src="https://panasonic.co.jp/design/flf/assets/img/works/doing_io/doing_io_white_main.jpg"></a>

<br><hr>

## 作り方
  
### 1 準備

- 必要なパーツを用意

<img width="500px" src="images/all_parts.jpg">

|     | 部品名     | 個数 |  販売リンク（例）         | 備考 |
|:----:|:---------|:----|:------------------------|:----|
|  1  | M5Stack Core2 | 1 |[スイッチサイエンス](https://www.switch-science.com/catalog/6530/) | |
|  2  | USB Type-Cケーブル | 1 | | M5Stack Core2 に付属 |
|  3  | M5Stack用赤外線送受信ユニット | 1 |[スイッチサイエンス](https://www.switch-science.com/catalog/5699/) | 一般的な赤外線受信センサを使ってもOKです |
|  4  | HY2.0 ケーブル (Groveケーブル) | 1 | | M5Stack用赤外線送受信ユニットに付属 |
|  5  | モバイルバッテリー ([BH-BZ40K](https://panasonic.jp/battery/products/mobile-battery/bh-bz40k.html)) | 1 | [Amazon](https://www.amazon.co.jp/dp/B0892JJ9K5) | お手持ちのモバイルバッテリーでもOKです |

★ 参考価格（総額） : 約5,500円 前後（モバイルバッテリー抜き）


### 2 配線 / 組み立て

1. M5Stack Core2 に Groveケーブルを接続します。

    <img src="images/core2_connect_cable.jpg" width="500px" />

1. 赤外線送受信ユニット と Groveケーブルを接続します。

    <img src="images/unit_connect_cable.jpg" width="500px" />

1. M5Stack Core2 に USBケーブルを接続します。

    <img src="images/core2_connect_usb.jpg" width="500px" />

1. USBケーブルとモバイルバッテリーを接続して完成です！

    <img src="images/battery_connect_usb.jpg" width="500px" />


### 3 開発環境のダウンロードとインストール

下記リンクを参考に開発環境をインストールしてください。

[M5Stack開発環境のダウンロードとインストール](https://github.com/panasonic-corporation/doingio-base-docs/blob/master/README.md#a-m5stack%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E3%81%AE%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E3%81%A8%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)

### 4 ファームウェアのダウンロード

1. ファームウェアをダウンロードしてください。

    https://github.com/panasonic-corporation/doingio-xmodal-aircon-speaker

    <img src="images/firmware_download.png" width="500px" />

1. プロジェクトを開いてください。

    ダウンロードしたフォルダを開き、doingio-xmodal-aircon-speaker/XModalAirconditionerSpeaker/XModalAirconditionerSpeaker.ino をダブルクリックしてArduino IDEで開きます。


### 5 ライブラリのダウンロードとインストール

1. ”スケッチ” → ”ライブラリをインクルード” → ”ライブラリを管理”「IRremoteESP」と検索して「IRremoteESP8266」をインストールしてください  

    <img src="images/irremoteesp8266.png" width="500px" />

1. ”スケッチ” → ”ライブラリをインクルード” → ”ライブラリを管理”「esp8266audio」と検索して「ESP8266Audio」をインストールしてください  
    <img src="images/esp8266audio.png" width="500px" />


### 6 Config.h の設定

1. Arduino IDEの右上の逆三角アイコンをクリックし、Config.hを選択します。

    <img src="images/arduino_select_config_file.png" width="500px" />

1. Arduino IDEでconfig.hを開き、**必要であれば**下記項目を修正します。
    - IR_PIN: 赤外線受信センサのピン番号
    - FONT_PATH: 使用するフォントのパス
    - LOGO_IMAGE_PATH: スプラッシュ画面のロゴ画像パス
    - HEAT_SOUND_DIR: 暖房のときに再生する音声ファイル(mp3)
    - COOL_SOUND_DIR: 冷房のときに再生する音声ファイル(mp3)
    - HEAT_COLOR: 暖房のときの画面背景色
    - COOL_COLOR: 冷房のときの画面背景色

    <img src="images/arduino_config.png" width="500px" />

### 7 書き込み

1. PCとデバイスをUSBケーブルで接続し、Arduino IDEの「ツール」タブを開き下記の通り設定します。

    <img src="images/arduino_tool_setting.png" width="300px" />

1. 「書き込み」アイコンをクリックしてArduinoにファームウェアを書き込みます。

    <img src="images/arduino_burn.png" width="300px" />

### 8 筐体（ケース）の作り方

筐体は皆さんのアイディアで自由に作ってみましょう！

ハッシュタグ #dio_product でTwitterやInstagramなどでどんどんシェアしてください。

今回はサンプルとして、調達が容易な材料で作れる筐体の作り方を紹介します。

<img width="500px" src="images/all_elements.jpg">

|     | 材料名 | 個数 |  販売リンク（例）         | 備考 |
|:----:|:---------|:----|:------------------------|:----|
|  1  | ブラシ・ペンシルスタンド| 1 |[無印良品](https://www.muji.com/jp/ja/store/cmdty/detail/4549337497672) |  |
|  2  | ベルクロテープ | 1 | |  |
|  3  | 両面テープ | 1 | |  |

1. ケースに合わせてベルクロテープをカットします

    <img src="images/cut_velcro.jpg" width="500px" />

1. 片方のベルクロテープをケースに貼り付けます

    <img src="images/case_stick_velcro.jpg" width="500px" />

1. M5Stack用赤外線送受信ユニットの大きさに合わせて両面テープをカットします

    <img src="images/cut_double_sided_tape.jpg" width="500px" />

1. M5Stack用赤外線送受信ユニットに両面テープを貼り付けます

    <img src="images/stick_double_sided_tape.jpg" width="500px" />

1. M5Stack用赤外線送受信ユニットをケースに貼り付けます

    （エアコンの側面に貼り付けたときに正面に向く方向に向けてください）


    <img src="images/stick_ir_unit.jpg" width="500px" />

1. ケースに電子部品を入れ込みます

    <img src="images/put_into_case.jpg" width="500px" />

1. エアコンにもう片方のベルクロを貼ります

    <img src="images/aircon_stick_verclo.jpg" width="500px" />

1. ケースを貼り付けて完成です！

    <img src="images/stick_case.jpg" width="500px" />

ケースにマスキングテープなどを貼ってデコレーションしてみるのもいいですね☆

<img src="images/case_deco_1.jpg" width="250px" />

<img src="images/case_deco_2.jpg" width="250px" />

<img src="images/case_deco_3.jpg" width="250px" />


### 9 使用方法

1. USBケーブルを電源に差すと起動します。

1. 画面中央のボタンをタップするとミュート、画面左の部分を上下にスライドすることで音量調節ができます。

    <img src="images/mute.jpg" width="500px" />

1. 暖房の信号を受け取ると「たき火」の音、冷房の信号を受け取ると「風鈴」の音、停止の信号を受け取ると音声が停止します。
