# easyrpg.org

Source code of the EasyRPG homepage at https://easyrpg.org


## Requirements

 - [ruby] >=2.7, version 3 is recommended
 - [nanoc] >=4.12
 - [tidy-html5]
 - [some gems]


## Source code

Homepage development is hosted by GitHub, project files are available in this
git repository:

https://github.com/EasyRPG/easyrpg.org


## Building the site

Install needed gems (choose one):

```bash
$ make install       # for building the site
$ make install-devel # for additional development and testing
$ make install-ci    # for CI server, skips stuff
```

This will install all needed gems in the `vendor/bundle` folder and provide
available commands in the `bin` directory. You can use `helper.bash` script
to add them to your `$PATH` and therefore make them available to your shell.
Alternatively, you may run commands with prefix, i.e. `bin/nanoc`.

```bash
$ source helper.bash
$ nanoc                 # to build the page
$ nanoc compile --watch # Automatically rebuild website on changes
$ nanoc view            # Make website available at http://localhost:3000
$ nanoc live            # Combination of last two commands
```

For convenience there is a `Makefile` provided:

```bash
$ make           # Compile website and view it
$ make compile   # Compile website
$ make all       # Clear, compile and check website
$ make check     # Check compiled website for problems
$ make clean     # Remove generated page
$ make distclean # Remove any generated files and bundled gems
```

For different environments, there are several changes in behaviour defined
(e.g. minifying of css/js, changed url), the environment variable `NANOC_ENV`
and CLI switch `-env=SomeEnv` can be used. Currently, options are: `default`
(used if not provided), `development`, `production`, `pr` and `netlify`.

## CI on netlify [![Netlify Status][netlify-img]][netlify-deploy]

Site is available in a namespace at https://easyrpg.netlify.app.
Pull request builds will be linked automatically after CI run.


## Bug reporting

Available options:

* File an issue at https://github.com/EasyRPG/easyrpg.org/issues
* Open a thread at https://community.easyrpg.org
* Chat with us via IRC: [#easyrpg at Libera Chat]
* Contact us at https://easyrpg.org/contact/


## License

The homepage is currently provided "as-is", we are currently not able to have
a common license for all files, as they have been cluttered over the years. We
are going to clear that up and hope to provide it under a Creative Commons
license later. We hope that this is in the intention of the original authors
and designers (see [issue #5] for reference).


### 3rd party software

Included are the following 3rd party software:

* jQuery - https://jquery.com - Copyright (c) JS Foundation and other contributors,
  provided under the MIT license

* jQuery EasyTabs plugin - https://os.alfajango.com/easytabs/ - Copyright (c)
  2010-2011 Steve Schwartz (JangoSteve), dual licensed under the MIT and GPL licenses

* Flurry jQuery Plugin - https://github.com/joshmcrty/Flurry - Copyright (c)
  2016 Josh McCarty, provided under the GPLv2 license

* Magnific Popup - http://dimsemenov.com/plugins/magnific-popup/ -
  Copyright (c) 2014-2016 Dmitry Semenov, provided under the MIT license

* Favicons have been processed by https://realfavicongenerator.net

* IRC contact page is provided by https://kiwiirc.com

[ruby]: https://www.ruby-lang.org
[nanoc]: https://nanoc.ws/
[tidy-html5]: http://www.html-tidy.org
[some gems]: Gemfile
[netlify-img]: https://api.netlify.com/api/v1/badges/697e9cfb-4ea6-4945-8ddd-9384735e0b0f/deploy-status
[netlify-deploy]: https://app.netlify.com/sites/easyrpg/deploys
[#easyrpg at Libera Chat]: https://kiwiirc.com/nextclient/#ircs://irc.libera.chat/#easyrpg?nick=rpgguest??
[issue #5]: https://github.com/EasyRPG/easyrpg.org/issues/5
