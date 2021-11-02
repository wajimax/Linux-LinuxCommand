# Linux-LinuxCommand
## インストールアプリケーション処理
### Pythonのsite-packagesの場所を確認
python -c "from distutils.sysconfig import get_python_lib; print get_python_lib()"


## データ処理
### 複数単語に一致させてGrep検索
grep -v -e abc -e def *

### WikiExtractorでWikipediaダンプファイルから文章データを取得
・WikiExtractor
https://github.com/attardi/wikiextractor

nohup python WikiExtractor.py -b 500K -o extracted jawiki-20181220-pages-articles.xml.bz2 &

### 指定した範囲の行を取得
cat text.txt | head -終了行 | tail -`expr 終了行 - 開始行 + 1`

## ネットワーク処理
### requirements.txtに記載のURLを順番にダウンロード
wget -i requirements.txt
