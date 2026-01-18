# aaah.run

This was originally a Hugo site at aaron.kriegman.net. Now it is a static site at aaah.run. Messing around with templates turned out to be totally not worth the time. I have left the skeleton of the Hugo site in this repo. I still use it to compile new posts from markdown to html, and you can still use the theme if you want. Old README below.

# aaron.kriegman.net

My website, with a simple Hugo theme based off of Lexi Hale's
[ʞ.cc](http://xn--rpa.cc/). I liked her website, but I wanted to write pages in
markdown and automate things like header generation, so I translated her site
structure into a Hugo theme, using her style sheet that she was nice enough to
share.

If you would like to use this theme, you can either

- clone this repo, `rm -r content/*`, and start editing with `hugo new ...`, or
- copy `themes/k.cc` into your Hugo website's `themes` folder and update
  `config.toml`.

Then, be sure to go into `themes/k.cc/static/css/serenity.css` and change the
background color.
