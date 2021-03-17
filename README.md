# random-splash-image
[![MELPA](http://melpa.org/packages/random-splash-image-badge.svg)](http://melpa.org/#/random-splash-image)

It randomizes Emacs's splash image on startup screen(GNU Emacs buffer).

# Screenshots
As below, the pictures changes without modifying config file.
![screenshot 1](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/ss1.png)
![screenshot 2](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/ss2.png)
![screenshot 3](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/ss3.png)
![screenshot 4](https://raw.githubusercontent.com/kakakaya/random-splash-image/master/ss4.png)

# How to use (config)
Make directory for your favorite pictures, and copy pictures to there.
```
mkdir $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no001_picture.png $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no{002-100}_picture.png $HOME/.emacs.d/splash-images
```
Then, write below to your init.el:
```
(require 'random-splash-image)
(setq random-splash-image-dir (concat (getenv "HOME") "/.emacs.d/splash-images"))
(random-splash-image-set)
```

# How to use(others)
If you want to open GNU Emacs buffer again, but with other picture, then kill GNU Emacs buffer and execute below command.
```
M-x random-splash-image-reopen-screen
```

# FAQ
- Q. My pictures don't appear! / GNU Emacs buffer disappeared after installation!
  - A. If used incorrectly, startup buffer might disappear. Try them:
    - Is random-splash-image-dir variable valid? Check by M-x describe-variable.
    - Can your picture opened by emacs? Try to open directly.

# TODO
- [x] Packaging
- [ ] Auto-Resize large picture(using display-monitor-attributes-list).
- [ ] Over-Network splash image(really need?)

# Other Language Manual:
- [English](README.md)
- [日本語](README.ja.md)
