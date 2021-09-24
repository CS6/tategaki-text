# 縦書きテキスト

縦書きテキストをいい感じに作るアドオン

## インストール

- 当リポジトリの Code > Download ZIP から zip ファイルをダウンロードし、blender のアドオンインストールにそのまま zip ファイルを読み込ませる。
- 【推奨】または、リリースの Assets から zip ファイルをダウンロードし、以下同略

## メニューの場所

- オブジェクトコンテキストメニュー(ビューポートで右クリックしたときに開くメニュー) > Tategaki Tools

## 機能

### 縦書きテキストに変換

- テキストオブジェクトから変換

### 行間・字間調整

- 行間・字間、自動カーニングの有無を調整する

### メッシュに変換

- 縦書きテキストオブジェクトを単一メッシュオブジェクトに変換

## todo

- [x] data api に置き換えて高速化
- [x] マージンの調整をあとからできるようにする
- [x] カーニング計算を保存しておいてマージンの調整を早くする
- [x] UI の実装
- [x] プロパティバリデータ実装(typedDict を使うようにしたので実質できた)
- [x] 縦書きテキストをメッシュへフリーズする機能
- [ ] 縦書きテキストをカーブへフリーズする機能
- [x] bug:テキストの内容によってメッシュへの変換が失敗する どこかで None が混ざってるけどどこだろう
  - 空白文字の TextCurve.to_mesh()を実行すると None が帰ってくるので None のときは空のメッシュに置き換える
- [ ] props から縦書きテキストオブジェクトの生成
