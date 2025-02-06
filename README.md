# fitbit Heart Rate Analysis

#概要

本プロジェクトでは、Fitbit で取得した心拍データを用いて LF/HF 比とストレス値を算出し、異なる区間でのストレス値を比較する Python スクリプトを提供します。本研究は、心拍データの分析を目的としています。

# 実験の目的

fitbit の心拍データを UTC から JST に変換し、適切な形式に整える。

各実験条件（色、味）における LF/HF 比を算出し、ストレス値を評価する。

2分間の心拍データを取得し、FFT を用いた周波数解析を実施する。

LF/HF 比とストレス指標を基に異なる条件間の比較を行う。

# 使用技術

Python 3

NumPy, Pandas

SciPy

Matplotlib

JSON データ処理



# 使用方法

1.　fitbitから取得したファイルのインポート

with open('ファイル名', 'r') as file:
    data = json.load(file)

2.　計測時間の打ち込み、計測開始時間を記入する

甘味

sweet_clear_start="10:41:00:sweet_clear"

sweet_red_start="10:50:00:sweet_red"

sweet_green_start="11:06:00:sweet_green"

sweet_blue_start="10:45:00:sweet_blue"

sweet_pink_start="10:54:00:sweet_pink"

sweet_yellow_start="10:58:00:sweet_yellow"

sweet_orange_start="11:02:00:sweet_orange"


3.  実験は二日で行ってるので、甘味と塩味、酸味と苦味でつかわないほうをコメントアウト
   
計測時間とtarget配列で使用しない溶液をコメントアウト

4.　実行


# 出力データ

experiment_analysis_results_with_min_median_max.csv

各実験条件の LF/HF 比およびストレス指標をまとめた CSV ファイル。

LFHF_<condition>_<name>.pdf

各条件の LF/HF 比の変化を示すグラフ。

Stress_<condition>_<name>.pdf

各条件のストレス指標の変化を示すグラフ。







著者

近畿大学 理工学部 情報学科 システムデザイン論研究室　田中真矢

