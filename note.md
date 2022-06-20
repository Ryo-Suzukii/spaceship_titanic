### 0617
- とりあえずグリッドサーチでCとrandom_stateを決めてみる．
- ペナルティはどうするか未定．これで終われなければやってみてもいいかも

### 06201
- 0才児がいるグループの生存率が高いことに注目しているかどうかを表す`Group_zero`を追加
- ~~なんも意味なかった~~

### 06202
- わざわざカラムを消す必要はないんじゃないかと思い消さないでやってみる
- KNNに渡せなかったから`PassengerId`だけそのままにしたけどこれ分割してるデータがあるからなんも意味ないね
- ～～missingってカラムの意味わからんくなってきたから消してみる
``` 
Best params: {'C': 4, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7947411668036155 
```

### 06203
- なんか`VIP`消したらACC上がるらしい
```
Best params: {'C': 1, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7950698438783895
```
- ガチで草

### 06204
- なんかお金使ったか使ってないかでもあがるらしい
```
Best params: {'C': 1, 'max_iter': 100, 'penalty': 'l2', 'random_state': 0, 'solver': 'lbfgs'}
Best Score: 0.7942481511914543
```

- 下がっちゃった（笑）