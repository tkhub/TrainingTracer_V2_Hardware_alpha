[TraningTracer Ver.2](https://rt-net.jp/products/traning-tracer2/)
の勝手改造版です。
![tracer](https://rt-net.jp/wp-content/uploads/2020/05/RT-Tracer.png)

## 改造・改良箇所
* 改造箇所
  * 一般的な3端子レギュレータの端子配置(Vin-GND-Vout)への対応
    * [スーパー3端子レギュレータ](https://akizukidenshi.com/catalog/g/g107178/)が使用でき、高電圧なLiPoバッテリーに対応可能
  * 逆電圧による3端子レギュレータ破壊防止のDiを追加
  * 改造用に各種電源とI2Cのピンアウトを設定
  * ディスコンになったBMX055のかわりにBNO055を搭載可能
    * ショートピンの設定(ハンダ盛り)が必要
  * 自励式ブザーの代わりに圧電スピーカーを搭載可能でより多彩な情報を通知可能
    * 自励式ブザーを使用時は直流阻止コンデンサのC5をショートすること
  * I2Cディスプレイ用コネクタの設定
    * [0.96インチOLEDディスプレイ](https://akizukidenshi.com/catalog/g/g112031/)のような追加ディスプレイによりより多くの情報をユーザーに通知可能
* 改良箇所
  * パイロットランプの追加
    * 電源入れっぱなしの防止
  * [バッテリー電圧計測のブレ対策にコンデンサC4を追加](https://github.com/rt-net/TrainingTracer_V2_Hardware/issues/1)
  * [回路図上のラベルとセンサの物理配置、ソフトの命名の整合性確保](https://github.com/rt-net/TrainingTracer_V2_Hardware/issues/2)
  * [プログラム書き込み中にモータが回転する問題の解決](https://github.com/rt-net/TrainingTracer_Hardware/issues/7)

## フォルダ構成

* 3d_cad_data
　トレーニングトレーサーの3DCADデータ
  STPファイルとIGSファイルで保存しています。
* 3d_print_parts
　トレーニングトレーサーの3Dプリント部品のデータ
  * TrainingTracer_Motor_Mount.stl
    トレーニングトレーサーのモータマウントの3Dモデルです。
  * TrainingTracerV2_Slider.stl
    トレーニングトレーサーのスライダーの3Dモデルです。
  * TrainingTracerV2_Wheel.stl
    トレーニングトレーサーのホイールの3Dモデルです。
* circuits
　トレーニングトレーサーの回路図とNucleoの追加工マニュアル
  * TrainingTracer
    * KiCadのプロジェクトフォルダ
  * old
    * TrainingTracerV2_circuit_rev1.0.pdf
    トレーニングトレーサーのメイン基板の回路図です。
    * TrainingTracer_marker_circuit.pdf
    トレーニングトレーサーのマーカーセンサ基板の回路図です。
  * TrainingTracer_PCB.pdf
    改造後の基板
  * TrainingTracer_SCH.pdf
    改造後の回路図
  * 出荷時のNucleoの追加工.pdf
    トレーニングトレーサーのNucleoボードに行った追加工の情報です。
    
## 開発について

本リポジトリはオープンソースですが、開発はオープンではありません。  
機能追加については社内のガイドラインを優先します。  
誤植や不具合の修正は常時受け付けています。詳しくは[コントリビューションガイドライン](https://github.com/rt-net/.github/blob/master/CONTRIBUTING.md)に従ってください。

## ライセンス

(C) 2020 RT Corporation \<support@rt-net.jp\>

各ファイルはライセンスがファイル中に明記されている場合、そのライセンスに従います。特に明記されていない場合は、Apache License, Version 2.0に基づき公開されています。  
ライセンスの全文は[LICENSE](./LICENSE)または[https://www.apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)から確認できます。
