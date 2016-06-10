# EXE6_TextEditor
各種テキストを編集できるようになるかもしれないツール

## 使い方
※開発中のプログラムなので危険です。必ずデータのバックアップを取った状態で使用してください。

* 動作確認環境はWindows10 + Python2.7.11 + PyQt4
* EXE6TextEditor.py と EXE6Dict.py を同じディレクトリに置きます
* `>python EXE6TextEditor.py` でGUIが開きます
* Fileメニューから対応しているデータを開きます
* テキストボックス内の文字列を書き換えてWriteボタンを押すとメモリ上のデータを書き換えます（元のファイルに影響はありません）
  * 元のデータ部分に上書きするので容量を超えた書き込みは出来ません。
  * 書き込むデータが元の容量より少ない場合は文字列の左を\x00で埋めます
* Saveボタンを押すと保存メニューが開き、書き換えたデータをファイルに保存できます

## ファイルの説明
### EXE6Dict.py
* 文字コードやアドレスの辞書

### EXE6TextDumper.py
* 辞書に基づいて全データをテキストに変換するプログラム
* 会話データの解析などに利用可能

### EXE6TextEditor.py
* 各種テキストを編集できるようになるかもしれないツール
* 現在対応しているデータ
  * マップ名
  * チップ説明文
  * エネミー名
  * ナビ名
  * キーアイテム名
  * ナビカス名

### EXE6Trans.py
* 辞書に基づいてバイナリとテキストを相互変換するツール
