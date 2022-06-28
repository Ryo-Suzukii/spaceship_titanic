# spaceship_titanic

## IDについて
それぞれ新しく行ったとき(submitをした後は必ず)，新たなファイルとして実行ファイルを分けて管理しています．
それぞれにidを割り振っていて関連のあるファイルはすべて同じidとなっています．
ファイルの前方にある数字がidとなっていて作成日時+同日に作成した何個目のファイルかでidを決めています．
- 06201 -> 6/21作成の一つ目
## ディレクトリ環境

- csv
  - {id}_{test}_prepared.csv
  - 特徴量エンジニアリングをしたcsvファイル
- Engineering
  - {id}_Engineering.ipynb
  - 特徴量エンジニアリングを行うJupyter Notebookファイル
- spaceship-titanic
  - 公式のtrain,testデータ
- submit
  - submit_{id}.csv
  - 提出する用のcsvファイル
- test
  - {id}_test.ipynb
  - モデルを使用して学習，testデータの予測を行う
- a.sh
  - git pushを1コマンドでするためのファイル
  - 本編には関係ない
- logistic.ipynb
  - まだディレクトリ分けしてないときのなごり
  - 一番最初のモデルはこれ
- note.md
  - したいことや気づいたことをidごとにメモしているノート
  - ここを見ながらそれぞれのファイルをみると変更点がわかる
- README.md
  - これ
- requrements.txt
  - 導入しているライブラリ一覧
- visualized.ipynb
  - データを可視化してどんな特徴があるか眺めるためにつかったファイル