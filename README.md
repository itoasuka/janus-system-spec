Janusシステム仕様書
=====================

[Janus](https://github.com/itoasuka/janus)のシステム仕様書です。Sphinxで作成されています。

ビルド
------

以下のコマンドでHTMLドキュメントを生成します。

```
make html
```

以下のコマンドでPDFドキュメントを生成します。

```
make latexpdf
```

以下のコマンドでオートビルドサーバが起動します。
ファイルをウォッチし、自動的にHTMLドキュメントを生成します。
ブラウザで閲覧している場合、自動的にリロードされます。

```
sphinx-autobuild source build/html
```

テーマのセットアップ
----------------------

Sphinx環境をセットアップする際、[Read the Docs Sphinx Theme](https://sphinx-rtd-theme.readthedocs.io/)もセットアップしてください。
pipを利用する場合、実行するコマンドは以下のようになります。

```
pip install sphinx_rtd_theme
```
