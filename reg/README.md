# 行列分解の正則化が予測精度に与える影響の調査

3位解法の中心的なアイデアは評価行列の行列分解を説明変数に使うことでしたが、分解する際に正則化している点が特徴的でした。
そこで、正則化の有無や強さが予測精度にどれくらい影響を与えるか調査しました。

## 調査結果

- [atmaCup振り返り会の資料](./atmaCup_15_lt_3rd.pdf)

## 実験に用いたコード

- [atmacup_15_marupuro_reg_svd.ipynb](./atmacup_15_marupuro_reg_svd.ipynb)
  - 資料4ページ目のグラフの「SVD (正則化なし)」の結果を得るためのノートブック。
  - sklearnのTruncatedSVDで評価行列を分解。
- [atmacup_15_marupuro_reg_ials.ipynb](./atmacup_15_marupuro_reg_ials.ipynb)
  - 資料4ページ目のグラフの「SVD (正則化あり)」の結果を得るためのノートブック。
  - iALSで評価行列を分解。
- [atmacup_15_marupuro_reg_nmf.ipynb](./atmacup_15_marupuro_reg_nmf.ipynb)
  - 資料4ページ目のグラフの「NMF (正則化なし)」「NMF (正則化あり)」の結果を得るためのノートブック。
  - sklearnのNMFで評価行列を分解。
- [atmacup_15_marupuro_reg_raw.ipynb](./atmacup_15_marupuro_reg_raw.ipynb)
  - 資料4ページ目のグラフの「生の評価行列」の結果を得るためのノートブック。
  - 分解せず、評価行列をそのまま説明変数に使う。
- [atmacup_15_marupuro_reg_ials_best_lr001.ipynb](./atmacup_15_marupuro_reg_ials_best_lr001.ipynb)
  - 学習率を下げて「SVD (正則化あり)」を学習し直すノートブック。
  - 資料9ページ目のリーダーボードのスコアを得るための提出用ファイルを作るのに使う。
- [atmacup_15_marupuro_reg_raw_best_lr001.ipynb](./atmacup_15_marupuro_reg_raw_best_lr001.ipynb)
  - 学習率を下げて「生の評価行列」を学習し直すノートブック。
  - 資料9ページ目のリーダーボードのスコアを得るための提出用ファイルを作るのに使う。
- [plot.ipynb](./plot.ipynb)
  - 資料用のグラフを生成するノートブック。
