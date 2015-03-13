# random-splash-image
<pre>Emacsの起動画面(*GNU Emacs*バッファ)の画像をランダムに変更します。</pre>
## 他言語版マニュアル:
英語版が最新のはずです。
- [English](README.md)
- [日本語](README.ja.md)

# 使い方(設定)
適当な場所にフォルダを作成し、ランダムで表示したい画像をその中に入れます。
Make dircetory for your favorite pictures, and copy pictures to there.
```
mkdir $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no001_picture.png $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no{002-100}_picture.png $HOME/.emacs.d/splash-images
```
そして、以下の内容をinit.elに書き込みます。
```
(require 'random-splash-image)
(setq random-splash-image-dir (concat (getenv "HOME") "/.emacs.d/splash-images"))
(random-splash-image-set)
```

# 使い方(その他)
<pre>もし、もう一度*GNU Emacs*のバッファを別の画像と共に表示しなおしたい場合、バッファを一度killしてから以下のコマンドを実行してください。</pre>
```
M-x random-splash-image-reopen-screen
```

# FAQ
- Q. 画像が表示されない! / インストールしたら<pre>*GNU Emacs*</pre>のバッファが表示されなくなった!
  - A. 正しく設定しないと起動時のバッファが表示されなくなったりします。以下を確認してください:
    - random-splash-image-dirは正しく設定しましたか？M-x desribe-variableで確認してみてください。
    - 表示しようとしていた画像を直接Emacsで表示できるか確認してください。

# TODO
- [] パッケージ化
- [] ネットワーク越しに画像フォルダを指定(必要？)

