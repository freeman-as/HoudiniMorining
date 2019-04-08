## Houdini VEX
よく使うVEXまとめ

---
### VEX  - EXPRESSION

- **$F**：フレーム番号を表す変数

- **ch()**
  指定したパラメーターを参照
  http://www.sidefx.com/docs/houdini/vex/functions/ch.html

  ```C++
  float ch(string channel)
  // - string: 参照先のパスを指定
  ```

- **`opinputpath()`**
  指定したノードに入力されたノードのパスを取得


