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
* ~~p.172，p.180で使っている気象庁のデータの最後に `2020,+0.47*,+0.70*,+0.25*` という行が追加されました。[HTML版](https://www.data.jma.go.jp/cpdinfo/temp/list/an_wld.html)によれば `*` は「1月から11月までの月平均気温の偏差をもとに算出した速報値」だそうです。そのうち `*` が外されると思いますが，これが付いているとRではNA（欠測値）扱いになるだけですが，Pythonでは全部文字列になってしまい，プロットできません。次のように打ち込んでからプロットしてください： `df['世界全体'] = df['世界全体'].str.replace('*', '', regex=False).astype(float)`~~ ←この件も気象庁側で直りましたのでもう大丈夫です。
* p.28 「最初は `http://` が補われて」：Google Chrome の次のバージョン（90）からは `https://` が補われることになるとのことです（[Chromium Blog 2021年3月23日](https://blog.chromium.org/2021/03/a-safer-default-for-navigation-https.html)）。
