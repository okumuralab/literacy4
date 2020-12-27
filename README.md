# 『［改訂第4版］基礎からわかる情報リテラシー』サポートページ

2020年11月6日発売です。

## リンク

* [技術評論社（紙版）](https://gihyo.jp/book/2020/978-4-297-11710-8)
* [技術評論社（電子版）](https://gihyo.jp/dp/ebook/2020/978-4-297-11711-5)
* [版元ドットコム](https://www.hanmoto.com/bd/isbn/9784297117108)
* [アマゾン（紙版）](https://www.amazon.co.jp/dp/429711710X)
* [アマゾン（電子版）](https://www.amazon.co.jp/dp/B08M8XXWNT)

## 訂正など

* ~~付録A（p.178）で `pd.read_excel('〜.xlsx')` となっているところは [xlrd パッケージの仕様変更](https://oku.edu.mie-u.ac.jp/~okumura/python/201212.html) のため今後は `pd.read_excel('〜.xlsx', engine='openpyxl')` とする必要があります（`openpyxl` がインストールされていなければ `pip install openpyxl` します）。~~ ←この件，pandas側で対応されたので，今まで通りの使い方で大丈夫です（`openpyxl` は必要です）。
