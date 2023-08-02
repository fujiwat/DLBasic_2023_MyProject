DL基礎講座2023 最終課題
# 誰でも良い結果が得られる、学習率 探索プログラム
### Author:  tfujiwara 藤原隆弘
 
このプログラムは、学習率を探索し、良い値を見つけることができます。（言語：Python）
## 利用した学習データ
DL基礎講座2023の第11回「変分オートエンコーダ（VAE）を用いてFasionMNISTの画像を生成してみましょう」で、検証しました。
学習速度によっては、試行回数を変える必要があるかもしれません。

## 実行環境
Google Colaboratory

## 紹介ビデオ
最終課題説明動画1080p.mp4

## 技術解説（提出文書）
tfujiwara20230801a.pdf

## ソースコードと実行結果
- FinalProj/notebooks には、Google Colab用の notebookファイルがあります。Colabのファイルは、実行結果も残っています。
- FinalProj_py/src には、Pythonのソースコードファイルがあります。（Google Colabから生成したもの）
各ソースコードファイルの役割は以下の通り。

### LR-Explorer Phase1.ipynb            lr_explorer_phase1.py
学習率探索プログラム。50エポック繰り返しながら、良い値の付近を桁を増やしながら探索します。
Phase1: 探索フェースの実行結果が入っています。
※時間がかかります。

### LR-Explorer Phase2 LR0.00038.ipynb  lr_explorer_phase2_lr0_00038.py
Phase2: 活用フェーズ。Phase1で得られた学習率 0.00038 を使って400エポック実行した結果が入っています。

### LR-Explorer Phase2 LR0.00041.ipynb  lr_explorer_phase2_lr0_00041.py
Phase2: 活用フェーズ。Phase1で得られた学習率 0.00041 を使って400エポック実行した結果が入っています。

### Cosine Annealing 50.ipynb           cosine_annealing_50.py
結果の比較用に用意した、コサインアニーリングによる学習率と検証結果を得るプログラム。（コサイン分割50回）

### Cosine Annealing 100.ipynb          cosine_annealing_100.py
結果の比較用に用意した、コサインアニーリングによる学習率と検証結果を得るプログラム。（コサイン分割100回）

### Cosine Annealing 200.ipynb          cosine_annealing_200.py
結果の比較用に用意した、コサインアニーリングによる学習率と検証結果を得るプログラム。（コサイン分割200回）

### Cosine Annealing 400.ipynb          cosine_annealing_400.py
結果の比較用に用意した、コサインアニーリングによる学習率と検証結果を得るプログラム。（コサイン分割400回）

### HandSearch LR0.0003.ipynb                      handsearch_lr0_0003.py
結果の比較用に用意した、手探り（通常の固定学習率でエポックを繰り返す）プログラム。学習率0.0003

## 備考
データは、東京大学 松尾研究室 DL基礎講座2023で提供されたものです。

## 参考
https://deeplearning.jp/lectures/deep-learning-foundation/ <br />
https://weblab.t.u-tokyo.ac.jp/deeplearning%E5%9F%BA%E7%A4%8E%E8%AC%9B%E5%BA%A7%E3%81%AE%E6%BC%94%E7%BF%92%E3%82%B3%E3%83%B3%E3%83%86%E3%83%B3%E3%83%84%E3%81%AE%E7%84%A1%E5%84%9F%E5%85%AC%E9%96%8B/
