# random-splash-image
<pre>It randomizes Emacs's splash image on startup screen(*GNU Emacs* buffer).</pre>

## Other Languare Manual:
- [English](README.md)
- [日本語](README.ja.md)

# How to use (configure)
Make dircetory for your favorite pictures, and copy pictures to there.
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
<pre>If you want to open *GNU Emacs* buffer again, but with other picture, then kill *GNU Emacs* buffer and execute below command.</pre>
```
M-x random-splash-image-reopen-screen
```

# FAQ
- Q. My pictures doesn't appear! / <pre>*GNU Emacs*</pre> buffer disappeared after installation!
  - A. If used incorrectly startup buffer might disapear. Try them:
    - Is random-splash-image-dir variable valid? Check by M-x describe-variable.
    - Can your picture opened by emacs? Try to open directry.

# TODO
- [] Packaging
- [] Over-Network splash image(really need?)

