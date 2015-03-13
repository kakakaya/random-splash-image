# random-splash-image
Emacsの起動画面(GNU Emacsバッファ)の画像を指定したフォルダの中からランダムに選択し、表示します。

## 他言語版マニュアル:
英語版が最新のはずです。
- [English](README.md)
- [日本語](README.ja.md)

# Screenshots
![screenshot 1](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/rsi-ss-1.png)
![screenshot 2](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/rsi-ss-2.png)

# 使い方(設定)
適当な場所にフォルダを作成し、ランダムで表示したい画像をその中に入れます。
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
もし、もう一度GNU Emacsのバッファを別の画像と共に表示し直したい場合、バッファを一度killしてから以下のコマンドを実行してください。
```
M-x random-splash-image-reopen-screen
```

# FAQ
- Q. 画像が表示されない! / インストールしたらGNU Emacsのバッファが表示されなくなった!
  - A. 正しく設定しないと起動時のバッファが表示されなくなったりします。以下を確認してください:
    - random-splash-image-dirは正しく設定しましたか？M-x desribe-variableで確認してみてください。
    - 表示しようとしていた画像を直接Emacsで表示できるか確認してください。

# TODO
- [ ] パッケージ化
- [ ] ネットワーク越しに画像フォルダを指定(必要？)

