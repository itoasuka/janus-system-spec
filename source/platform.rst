稼働プラットフォーム
----------------------

Janusは、「さくらのVPS」の「512MBプラン」に同サービスで標準で用意されている「Ubuntu Server 18.04」をOSとしてセットアップした
サーバー上で稼働するようになっています。

============== ============================================
項目           採用しているもの
-------------- --------------------------------------------
サーバ形態     さくらのVPS 512MBプランを利用
OS             Ubuntu Server 18.04\ [#os]_
MTA            Postfix\ [#pkg]_
HTTP サーバ    Nginx\ [#pkg]_
FTP サーバ     vsftpd\ [#pkg]_
SSH サーバ     OpenSSH\ [#pkg]_
RDBMS          PostgreSQL\ [#pkg]_
============== ============================================

さくらのVPSのコントロールパネルよりUbuntu Server 18.04をセットアップする際に設定したイニシャルユーザの情報は以下のとおりです。

============== ======================
項目           設定値
-------------- ----------------------
ユーザ名       ``ubuntu``
パスワード     ``M,LyWIyH+4``
============== ======================

その他のパスワードの設定等は、「Janus運用マニュアル」を参照してください。


.. [#os] さくらのVPSで標準で選択可能なOSのひとつ

.. [#pkg] Ubuntu Server 18.04の標準パッケージを使用
