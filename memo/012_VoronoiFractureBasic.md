## 012_VoronoiFractureBasic
プロジェクトの説明

---
### メモ

- ボロノイ分割
  基準点をもとに分割する方法で、近接する2点の二等分線によって領域が区切られる
  「分割のための基準点」が必要
- `Scatter`はポリゴンモデルだと中身が空洞なので表面のみにポイントが配置される
- ボリューム：不定形物を表現する際に用いる、中身の詰まった形式
- `RBD Object`
  基本的に一個のRBD Objectを作成するもので、複数の破片の挙動には向いていない
- `RBD Fractured Object`
  破片を個別にシュミレーションできる
- 



------

### 使用したノード (抜粋)

- **``Scatter(SOP)``**
  入力したジオメトリにポイントを配置する
- **``Voronoi Fracture(SOP)``**
  ボロノイ分割を行う
- **``Exploded View(SOP)``**
- **``Voronoi Fracture(SOP)``**
  ボロノイ分割を行う
- **``RBD Fractured Object(DOP)``**
  複数のRBD Objectを作成できる
  破片を個別にシュミレーションできる
- **``RBD Packed Object(DOP)``**
  パックプリミティブを使ってRBDオブジェクトを作成できる
- **``Assemble(SOP)``**
  バラバラに分割されたジオメトリを個別の破片として扱えるように必要な処理を行う
- 
