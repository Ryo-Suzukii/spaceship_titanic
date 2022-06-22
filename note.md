### 0617
- とりあえずグリッドサーチでCとrandom_stateを決めてみる．
- ペナルティはどうするか未定．これで終われなければやってみてもいいかも

### 06201
- 0才児がいるグループの生存率が高いことに注目しているかどうかを表す`Group_zero`を追加
- ~~なんも意味なかった~~

## 06202
- わざわざカラムを消す必要はないんじゃないかと思い消さないでやってみる
- KNNに渡せなかったから`PassengerId`だけそのままにしたけどこれ分割してるデータがあるからなんも意味ないね
- ～～missingってカラムの意味わからんくなってきたから消してみる
``` 
Best params: {'C': 4, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7947411668036155 
```

## 06203
- なんか`VIP`消したらACC上がるらしい
```
Best params: {'C': 1, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7950698438783895
```
- ガチで草

## 06204
- なんかお金使ったか使ってないかでもあがるらしい
```
Best params: {'C': 1, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7942481511914543
```

- 下がっちゃった（笑）

## 06211
- 学習アルゴリズムをロジスティック回帰からXGClassifierに変えてみた．
- グリッドサーチでパラメータ見つけてtestデータ突っ込んだら0.8超えた！！
```
Best params: {'eval_metric': 'mlogloss', 'learning_rate': 0.1, 'n_estimators': 50}
Best Score: 0.8059161873459326

```

- ついでにグリッドサーチのパラメータ増やしたらもっと上がった！！！！

```
Best params: {'eval_metric': 'mlogloss', 'learning_rate': 0.05, 'max_depth': 5, 'n_estimators': 100}
Best Score: 0.8085456039441249
```

- submit結果は`0.73275`
- 過学習かぁ....

## 06212

- パラメータ増やした
```
Best params: {'colsample_bytree': 1.0, 'eval_metric': 'mlogloss', 'learning_rate': 0.1, 'max_depth': 5, 'min_child_weight': 2, 'n_estimators': 50, 'subsample': 1.0}
Best Score: 0.809202958093673
```

- `0.72246` もう0.795で妥協しようかな