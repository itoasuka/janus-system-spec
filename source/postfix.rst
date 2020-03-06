Postfixの構成
--------------

JanusではMTAとしてPostfixを使用しています。

SPFのサポート
^^^^^^^^^^^^^^^

JanusではMTAでSPFチェックが行われていることを期待しています。
Ubuntu Server 18.04におけるspfサポートのセットアップの手順の一例を説明します。

まずSPFサポートパッケージをインストールします。

.. code-block:: shell

   $ sudo apt install postfix-policyd-spf-python

``/etc/postfix/master.cf``\ に以下のように追記します。

.. code-block:: text

   policyd-spf unix - n n - 0 spawn
     user=nobody argv=/usr/bin/policyd-spf

``/etc/postfix/main.cf``\ にこのポリシーが適用されるように記述します。

.. code-block:: text

   smtpd_recipient_restrictions =
       permit_mynetworks,
       check_policy_service unix:private/policyd-spf,

   policy_time_limit = 3600


aliasesの設定
^^^^^^^^^^^^^^^

Janusは、MTAのaliasesファイルでメールフィルタとして設定されることを想定されています。
``renkei@tk2-212-15881.vs.sakura.ne.jp``\ でメールを受け取る場合、\ ``/etc/aliases``\ に以下のように追記します。

.. code-block:: text

   renkei: "| /usr/local/bin/janus"

追記後\ ``newaliases``\ コマンドを実行してください。

.. code-block:: shell

   $ sudo newaliases


