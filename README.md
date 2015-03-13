# random-splash-image
It randomizes Emacs's splash image

# How to use
Make dircetory for your favorite pictures, and copy pictures to there.
```
mkdir $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no001_picture.png $HOME/.emacs.d/splash-images
cp $HOME/Pictures/my_no{002-100}_picture.png $HOME/.emacs.d/splash-images
```
Then, write below to your init.el:
```
(setq splash-image-dir (concat (getenv "HOME") "/.emacs.d/splash-images"))
```

# TODO
* Packaging
* Over-Network splash image(really need?)

