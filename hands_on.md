# データ分析環境について

## PC Spec
CPU : Core i9-9900K 8Core 12threads 3.6GHz  
GPU : RTX 2080  
OS : Ubuntu 20.03  
Desktop Manager : LXDE

## インストール済みソフトウェア
* Python3.6
  * 機械学習関連: tensorflow-gpu=2.6 sklearn
  chainer pandas-ml
  * 統計分析: statsmodels matplotlib seaborn ggplot
  * 数値計算: pandas numpy scipy
  * その他: nltk datetime xlde lxdr
* Python2.7
* Jupyter-notebook
* R
* スプレッドシート(WPS)
* パワーポイント(WPS)
* ドキュメント(WPS)

その他必要なものがあった場合は管理者へ連絡して下さい。

## 作業開始方法と注意
### 作業について
* `data`フォルダは、提供データの格納先&読み込みのみに使ったほうがいいと思います。
* 各自作業スペースはworkspaceフォルダ内に、自分専用フォルダを作るのがいいと思います。
* **Jupyter notebookを使用する場合は、checkpointが他の人と衝突する可能性があるので、作成した自分専用フォルダを起点に起動して下さい。**

### セキュリティ
* 作業中に作られたファイル（分割や分析結果、グラフなど）は必ずworkspaceフォルダの中に保存するようにして下さい。
* クリップボードの転送はできません。作業環境内のみでのコピー&ペーストは可能です。

## Jupyter-notebook起動
1. ターミナルを起動  
`左下メニュー` → `System Tools` → `LXTerminal`

2. 以下コマンドで自分の作業ディレクトリへ移動してから起動
```bash
cd
cd Desktop/workspace/自分専用フォルダ名
jupyter-notebook
```
3. ブラウザ起動して開きます。`New`タブで作業開始します。

4. 作業が終わったら保存し、右上の`Quit`を押してからブラウザを閉じるようにしてください。そのままにするとメモリを無駄に食ってしまうのでご協力を。

## R
ターミナルでRと入力するか、`メニュー`→`Graphics`→`R`から起動します。

## エクセル（っぽいやつ）
`menu`→`WPS Office`→ `WPS Spreadsheets`
