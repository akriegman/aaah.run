# aaah.run

This was originally a Hugo site at aaron.kriegman.net. Now it is a static site at aaah.run. Messing around with templates turned out to be totally not worth the time. I have left the skeleton of the Hugo site in this repo. I still use it to compile new posts from markdown to html, and you can still use the theme if you want. Old README below.

Update: I have added a script for syncing pages from notion. I want writing to be easy and seamlessly synced between my devices. Notion has some cool innovations, like having documents contain other documents instead of having folders. It's probably overpowered for this though. We'll see if I regret this.

Some notes on quirks of this pipeline:
- multimarkdown turns `$...$` into `\(...\)`. not ideal, but I've just changed the template to tell katex to look for this... if there's a way to tell mmd to leave $ alone I would prefer that.
- notion turns $$...$$ into inline math, which notion-to-md turns into `$...$`. I could use `\[...\]`, but mmd expects `\\[...\\]` which I do not want to deal with. what we can do however is use notion equation blocks. i'm kinda fine with using plaintext for inline math and notion features for display math. hopefully it doesn't get confusing...
- there are three ways to make a table without a header in markdown:
  - leave the header empty, and use css that makes the empty header row invisible. works with most md implementations, but is fragile, especially if you sometimes do want a header row.
  - use multimarkdown and do not write a header row
  - use pandoc and leave the header row empty. pandoc will omit the header altogether in the output.
  the last two options are both viable, but they will require getting notion-to-md to respect the notion header row toggle. which notion-to-md honestly should do by default. the best resolution is if notion-to-md outputs an empty heder row by default and I switch to pandoc.

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
