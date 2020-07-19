## [説明] 
キーからTOTPを生成して、入力してくれるやつです。
モジュール流用しただけだし、電通大生しかみてないんでUEC 2FACTORなんとかって名づけました。

windows以外の人は自力で頑張ってね☆

## [使い方] 
1.Python3系をインストール（してある人は2へ）
https://www.python.jp/install/windows/install_py3.html<br>
そのまま従って

2.pyotpモジュールとpyautoguiモジュールをインストール(してある人は３へ）
「pip3 install pyotp」と「pip3 install pyautogui」をコマンドライン上で実行するだけ

3.環境変数「UEC_2FACTOR_PRIVATEKEY」に秘密鍵設定
https://www.cc.uec.ac.jp/ug/ja/account/index.html#uec-account-2fa<br>
からトークンアプリを利用する→パスワード変更ページ→ログイン→二段階認証→URIのsecret=から&issuer~の間をコピー
この値をUEC_2FACTOR_PRIVATEKEYとして環境変数に登録してください。
絶対に予備のためにgoogleのAuthenticatorとかにも登録しといてね。

4.totp.pyを保存して、保存したディレクトリで「python3 totp.py」ってやったらカーソルがあるところにパスワードが自動入力されます。実行してから入力されるまで時間を空けたい人はtimeモジュールでもインポートして自分でやってね。
https://techplay.jp/column/575<br>
こんな面倒なことするより、ショートカットキー割り当てた方がいい気がするけど
それどうやってやるんだよハゲってひとは、run.vbsとdo.batをtotp.pyと同じディレクトリに入れてrun.vbsのプロパティを開いてショートカットキー割り当てておしまい。

## [文句] 
・pythonインストールするの面倒<br>
→あきらめましょう

・実行可能ファイルを見せろ<br>
→python布教したいのでいやだ

・よくわからんから代わりに全部やれ<br>
→ハーゲンダッツと引き換え
<br>
## [追記]
・do.batがセキュリティ上危険ってことで削除されるぴえん（7/19 15:35）<br>
→確かに。中身コピペして自分で作ってね（ごめん）<br>

・do.batないけど？(07/19 22:05)<br>
→do.batいらないアップデートしたので削除しました。<br>

・ショートカットキー反応しない！(07/19 22:05)<br>
→再起動すると反映されるそうです！ありがとうNさん<br>

・ハーゲンダッツきつい(07/19 22:05)<br>
→LINEしてくれたら考える（Kさんは２つもらう）<br>

・Python反応しない！(07/19 22:05)<br>
→microsoft storeのpythonが開いてる場合があります。「where python3」ってやってpythonの実行可能ファイルが置いてあるところ直に参照してね。<br>