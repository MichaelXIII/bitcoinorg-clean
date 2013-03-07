# Requirements

Installing dependencies

    sudo apt-get install rubygems
    sudo gem install jekyll aquarium json less therubyracer

# Usage

* update DOWNLOAD\_VERSION in _config.yml
* run ./_contrib/updatesitemap if you changed pages
* run jekyll
* output will be in \_site/

# Translation

* Find the two letter ISO 639-1 code for your language (fr, en, jp)
* Run ./_contrib/translate (language code) (language name)
* Rename html files in (lang)/ according to your language. And update links in _layouts/base-(lang).html and (lang)/*.html to reflect your changes.
* Translate all .html and images files in (lang)/ and _layouts/base-(lang).html
* A tips for translators, you can preview your work in a simple Google chrome browser with no HTTP server. Just go to the existing english page, open the javascript console with CTRL + SHIFT + J and use the following command to make the page editable : document.body.contentEditable=true

## Advanced Usage

### Alerts

You can easily put alerts on the website by changing the ALERT and ALERT\_CLASS variables in each base-*.html layout.

Example:

```
ALERT_CLASS: error
ALERT: <strong>Security alert:</strong> Please upgrade to 0.3.25 as soon as possible!
```

will produce a red alert box. Possible classes are: error (red), info (blue), success (green) and warning (yellow)

### Release Notes

Release notes should be placed in `_posts/releases/YEAR-MONTH-DAY-SHORTTITLE.md` and adhere to this format:

```
---
layout: post
title: Bitcoin version 0.3.24 released
src: http://sourceforge.net/mailarchive/message.php?msg_id=27771039
category: releases
---

Bitcoin v0.3.24 is now available for download at
<https://sourceforge.net/projects/bitcoin/files/Bitcoin/bitcoin-0.3.24/>

...
```
* `SHORTTITLE` is used to construct the URL. Something like `v0.3.24` will be fine
* `layout: post` important for Jekyll
* `title: ...` will be used as the title
* `src: ...` (optional) link to full annoucement
* `category: ...` category of post
** `releases`
** `events`

### Aliases for contributors

Aliases for contributors are defined in ```_config.yml```.

```
aliases:
  s_nakamoto: Satoshi Nakamoto
  --author=Satoshi Nakamoto: Satoshi Nakamoto
  gavinandresen: Gavin Andresen
```

# Requirements

These ruby gems are required to build the website:

* jekyll
* aquarium
* json
* less
* therubyracer

