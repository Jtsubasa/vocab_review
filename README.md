## 単語復習プログラム (Vocab Reviewer)

このリポジトリは、CSVファイルから単語と意味、カテゴリーを読み込み、GUI 上で復習問題を出題する Python プログラムです。

---
### ファイル構成

- `vocab.csv`  
  語彙データを保存する CSV ファイル。以下の形式で管理します。
  ```csv
  word,meaning,category
  apple,りんご,名詞
  run,走る,動詞
  ...
  ```

- `history.txt`  
  セッション中の出題履歴を保存するテキストファイル。プログラム終了時に自動生成・上書きされます。

- `vocab_reviewer.exe`  
  メインの実行ファイルです。

- `README.md`  
  本ファイル：プログラムの概要と使用方法を記載しています。

---
### インストール・実行手順

1. このリポジトリをクローンまたはダウンロード。
2. zipファイルを展開
3. vocab_reviewer.exeを実行(ウイルスソフトは無視)
4. 必要あればvocab.csvを編集

---
### 使い方

1. **カテゴリー選択**  
   ドロップダウンから出題したいカテゴリーを選択します。
   - **All**: 全カテゴリーから出題
   - その他: 各カテゴリーごとに出題

2. **出題 & 回答**  
   - 「次に」ボタンで新しい単語が表示されます。
   - 意味をエントリ欄に入力し、「提出」ボタンを押します。
   - 正解の場合は「正答: x / y」にカウントされ、意味が青文字で表示されます。

3. **履歴確認**  
   - 「履歴を見る」ボタンで、単語・入力回答・正解・正誤マーク（o/x）を一覧表示します。

4. **終了 & 履歴保存**  
   - 「終了」ボタンでウィンドウを閉じ、`history.txt` に履歴が保存されます。

---
### ファイル形式について

- **`vocab.csv`**
  - カラム順: `word, meaning, category`
  - 3列目の `category` は任意の文字列（例: 名詞, 動詞, 英熟語 など）

- **`history.txt`**
  - 出題終了時に自動生成
  - フォーマット: `単語,ユーザー回答,正解,correct/ wrong`
