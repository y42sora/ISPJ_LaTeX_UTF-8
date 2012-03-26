#情報処理学会(ISPJ)LaTeXスタイルファイル By UTF-8
[情報処理学会](http://www.ipsj.or.jp/index.html)の論文誌ジャーナルの[LaTeXスタイルファイル](http://www.ipsj.or.jp/journal/submit/style.html)がsjisだったので、UTF-8に変更し、かつ章ごとに個別ファイルにわけた物になります。

また、現在配布元のは私の環境では何故か紙の大きさが縦になってしまい左半分しか表示されないので、ちゃんと出力される物を使っています。

#ファイル構成
論文を書くためにはsrcの中にあるファイルだけ書き換えれば大丈夫です。

具体的なファイル構成は

+ sample.tex メインファイルだけど定義だけで基本そのまま
    + body.tex 論文本体の外部ファイルを読み込む所、章の追加とかはここに。
        + title.tex タイトル、著者名
            + abstract.tex 概要
        + section_1～5.tex 本文の各章
        + thebibliography.tex 参考文献リスト
        + appendix.tex 付録
        + biography.tex 著者情報

となっています。


#TODO
ファイル指定が全てsample.texからの相対パスになっているので、body.texからでもsrc/title.texと指定しなければならない。
現在のパスを変更するのをsample.texのbodyの呼び出し前後に入れたいんだけど…