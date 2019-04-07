## 008_increase_particles
プロジェクトの説明

---
### メモ

- `POP location`
  `Impulse Activation` : ノードが一回計算されるごとにパーティクルを生成する設定
  `Impulse Count` : ノードが一回計算されるごとに作成されるパーティクル数
  `Const. Activation` : 1秒あたりに放出されるパーティクルのオンオフを制御。0でこの設定での生成をしない
  `Life Expectancy` : パーティクルの寿命。単位は秒

- パーティクルのアトリビュート
  `dead` : 消滅したかどうかの値。デフォルトは0で、1になった瞬間に消滅
  `age` : パーティクル発生からの時間。単位は秒
  `life` : パーティクルが存在していられる時間。単位は秒
  ageがlifeを超えた瞬間にdeadが1になる

- `POP Solver`
  `Update/Reap At Frame End`
  オフにするとdead==1になった次のフレームで消失する

- `POP Replicate`
  パーティクルからパーティクルを発生
  `Shape/Shape`：Pointにするとパーティクルの位置から発生する
  `Attributes/Initial Velocity`：Set initail velocityにすると初期速度を自分で指定できる設定

- 新しくストリームが作成されると、その下にコネクトされているノードはそのストリーム内だけで有効で、別ストリームに分かれた時点で他のストリームにあるノードの影響を受けなくなる

- 基本的にストリームは名前依存なので、名前が同じものは同じストリームになる

- 