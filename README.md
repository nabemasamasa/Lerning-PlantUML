# Lerning-PlantUML
学習用

## 参考にしてるぺーじ

- [PlantUML Cheat Sheet](https://qiita.com/ogomr/items/0b5c4de7f38fd1482a48)
- [Visual Studio CodeでER図作成](https://qiita.com/kazuho39/items/99ed95efdcf3444b02a0)
- [PlantUMLでER図を描く！](https://medium.com/veltra-engineering/how-to-draw-er-diagram-with-plantuml-86ec2095645e)

## 確認してみたいこと

- 複数のファイルを管理している場合、参照とかどうするの？
- 論理名、物理名の組み合わせを見やすくしたい
- 列に対する装飾を列挙しておきたい
- レイアウト系を見やすいように整えたい場合どうするんだろう、順番とか…？
- テーブルの列から参照を生やせないかな…

## 学んだこと

### 環境設定

windows10 64bit

1. Java
  - Install済みなので不要だった
2. [Graphviz](http://www.graphviz.org/)いれる
  - `Windows`の`Stable and development Windows Install packages`
3. VSCode Extensionsを入れる
  - [PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
  - VSCoodeはv1.40

### かんたんなつかいかたをざつにかく

※ファイル名とか、変数は頭に$

- `@startuml $PackageName`と`@enduml`でひとつの組み合わせ
- `entity "M_USER" {}`で1テーブルにからっぽのエンティティ
- `--`でエンティティの中に一本線
- `==`でエンティティの中に二重線
- `$entityname }-{ $entityname`で三本生えた参照
- `$entityname -{ $entityname`でsrcからdstへ一方的な参照
- `column [PK]`みたいな感じで後ろに属性付けられる
- `+`とか、``
- シングルクォーテーションで囲めば1行コードコメント的なのを書ける
- PNGはデフォルトoutフォルダへ.puとか.pumlとかのファイル名.pngとかで出力される
  - 一応、コマンドパレットや右クリックでダイアグラムの出力からできる
  - なので、リポジトリ直下の.vscodeフォルダにsettings.jsonとかtask.jsonとかでショートカットに設定しとくと捗るかも
