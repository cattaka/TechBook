## 自分の原稿をhtml化

    review-compile --target=html takao.re > takao.html

もしくは

    rake clean html re=takao.html

で takao.html が生成されます。

## 全員の原稿を html 化

    rake clean html_all

で *.re に対して *.html が生成されます。

## 全員の原稿を pdf 化

pdf を生成する場合は TeX のインストールが必須です。

    rake clean
    rake

で TechBook.pdf が出来ます(1行ですませたい場合は `rake clean pdf`)。

中では

    rm -f TechBook.pdf
    rm -rf TechBook/
    review-pdfmaker config.yml

のようなことしているらしいです(rake が使えない場合はこっち？)。


## Mac の場合

* sudo gem install review で ReVIEW をインストール
* http://tug.org/mactex/ から MacTeX.pkg をダウンロードしてインストール(pdf生成をしない場合は不要です)
