# 小望遠鏡実習：M57 の実測データから 50cm 望遠鏡での写りを予測する

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hsameshima/SmallTelescope_test01/blob/main/notebooks/m57_practicum.ipynb)

2026年10月8日にミューロン210（口径 210 mm）＋ ZWO ASI183MM で撮影した M57（環状星雲）のデータを使い、国立天文台 50cm 公開望遠鏡で同じカメラを使ったときの画素スケール・信号・S/N を予測して、本番の観測スケジュールを作る課題です。

## 使い方

1. 上の「Open in Colab」ボタンを押す
2. Colab のメニューで「ファイル → ドライブにコピーを保存」を選び、自分用のコピーを作る
3. 上のセルから順に実行し、`# TODO` のセルと「答え」のセルを埋める
4. 「ファイル → ダウンロード → .ipynb をダウンロード」で提出する

データはノートブックの最初のセルで自動的にダウンロードされます。

## 内容

| パス | 内容 |
| --- | --- |
| `notebooks/m57_practicum.ipynb` | 課題のノートブック |
| `data/20261008/` | 2026-10-08 の FITS（Light: Ha, O3, S2, R, G, B 各 2 枚、Dark 2 枚。60 秒、Bin4、gain 111） |

## 課題の構成

1. 画素スケールと視野（星のペアから実測し、50cm に換算）
2. 信号とノイズの実測（ペア差分、ゲイン、M57 のリングの信号）
3. 50cm での信号の換算（1 画素あたり・角度面積あたり、F 値の役割）
4. S/N と必要積分時間の予測
5. M57 の観測可能時間と当日のスケジュール
6. 予測の限界
