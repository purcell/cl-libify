[![Melpa Status](http://melpa.org/packages/cl-libify-badge.svg)](http://melpa.org/#/cl-libify)
[![Melpa Stable Status](http://stable.melpa.org/packages/cl-libify-badge.svg)](http://stable.melpa.org/#/cl-libify)
<a href="https://www.patreon.com/sanityinc"><img alt="Support me" src="https://img.shields.io/badge/Support%20Me-%F0%9F%92%97-ff69b4.svg"></a>

# Update Emacs Lisp code to use cl-lib instead of cl

`cl` is a deprecated library, and elisp authors should use `cl-lib`
instead.  In most cases, this is a matter of requiring "cl-lib" and
adding a "cl-" prefix to symbols that came from "cl".

This library provides an interactive command, `cl-libify`, which
replaces usages of "cl" symbols with their "cl-lib" equivalent,
optionally prompting for each

Note that some cl functions do not have exact replacements,
e.g. `flet`, so further code changes might still be necessary.

You can also use `cl-libify-mark-cl-symbols-obsolete` to mark old `cl`
names as obsolete, so that the byte compiler will help flag their use.

## Installation

### Manual

Ensure `cl-libify.el` is in a directory on your load-path, and
add the following to your `~/.emacs` or `~/.emacs.d/init.el`:

``` lisp
(require 'cl-libify)
```

### MELPA

If you're an Emacs 24 user or you have a recent version of
`package.el` you can install `cl-libify` from the
[MELPA](http://melpa.org) repository. The version of
`cl-libify` there will always be up-to-date.

See the command `cl-libify`.

## About

Author: Steve Purcell <steve at sanityinc dot com>

Homepage: https://github.com/purcell/cl-libify

This little library was extracted from the author's
[full Emacs configuration](https://github.com/purcell/emacs.d), which
readers might find of interest.

<hr>

[💝 Support this project and my other Open Source work](https://www.patreon.com/sanityinc)

[💼 LinkedIn profile](https://uk.linkedin.com/in/stevepurcell)

[✍ sanityinc.com](http://www.sanityinc.com/)

[🐦 @sanityinc](https://twitter.com/sanityinc)
