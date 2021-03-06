SFDC Dev Config
======

SFDC Dev Config is a script to set up an macOS laptop for Salesforce.com development. 
It has been forked from the Laptop script (https://github.com/thoughtbot/laptop)

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Requirements
------------

We support:

* macOS Mavericks (10.9)
* macOS Yosemite (10.10)
* macOS El Capitan (10.11)
* macOS Sierra (10.12)

Older versions may work but aren't regularly tested. Bug reports for older
versions are welcome.

Install
-------

Download, and execute the script:

```sh
curl -LOk https://github.com/dmgerow/sfdc-dev-config/archive/master.zip && unzip master.zip && cd sfdc-dev-config-master && sh mac 2>&1 | tee ~/sfdc-dev-setup.log
```

Debugging
---------

Your last script run will be saved to `~/sfdc-dev-setup.log`.
Read through it to see if you can debug the issue yourself.
If not, copy the lines where the script failed into a
[new GitHub Issue](https://github.com/dmgerow/sfdc-dev-config/issues/new) for us.
Or, attach the whole log file as an attachment.

Getting this error? 

```sh
chsh: /usr/local/bin/zsh: non-standard shell
```

Run 
```sh
sudo vim /etc/shells
```

Add the following line to the end of your shells file:
```sh
/usr/local/bin/zsh
```

Or this error when trying to use rbenv?
```sh
 /usr/local/Cellar/rbenv/1.0.0/libexec/rbenv: No such file or directory
```
Find the solution here: https://coderwall.com/p/0o64yq/rbenv-issues-when-switching-to-zsh

What it sets up
---------------

macOS tools:

* [Homebrew] for managing operating system libraries.

[Homebrew]: http://brew.sh/

Unix tools:

<!-- * [Exuberant Ctags] for indexing files for vim tab completion -->
* [Git] for version control
* [OpenSSL] for Transport Layer Security (TLS)
<!-- * [RCM] for managing company and personal dotfiles -->
<!-- * [The Silver Searcher] for finding things in files -->
<!-- * [Tmux] for saving project state and switching between projects -->
* [Zsh] as your shell

<!-- [Exuberant Ctags]: http://ctags.sourceforge.net/ -->
[Git]: https://git-scm.com/
[OpenSSL]: https://www.openssl.org/
<!-- [RCM]: https://github.com/thoughtbot/rcm -->
<!-- [The Silver Searcher]: https://github.com/ggreer/the_silver_searcher -->
<!-- [Tmux]: http://tmux.github.io/ -->
[Zsh]: http://www.zsh.org/

Heroku tools:

* [Heroku Toolbelt] and [Parity] for interacting with the Heroku API

[Heroku Toolbelt]: https://toolbelt.heroku.com/
[Parity]: https://github.com/thoughtbot/parity

GitHub tools:

* [Hub] for interacting with the GitHub API

[Hub]: http://hub.github.com/

<!-- Image tools: -->

<!-- * [ImageMagick] for cropping and resizing images -->

<!-- Testing tools: -->

<!-- * ~~[Qt] for headless JavaScript testing via Capybara Webkit~~ -->

<!-- [Qt]: http://qt-project.org/ -->

Programming languages and configuration:

* [Bundler] for managing Ruby libraries
* [Node.js] and [NPM], for running apps and installing JavaScript packages 
* [Rbenv] for managing versions of Ruby
* [Ruby Build] for installing Rubies 
* [Ruby] stable for writing general-purpose code 

[Bundler]: http://bundler.io/
[ImageMagick]: http://www.imagemagick.org/
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[Rbenv]: https://github.com/sstephenson/rbenv
[Ruby Build]: https://github.com/sstephenson/ruby-build
[Ruby]: https://www.ruby-lang.org/en/

Databases:

* [Postgres] for storing relational data
* [Redis] for storing key-value data

[Postgres]: http://www.postgresql.org/
[Redis]: http://redis.io/

Salesforce:

* [Ant] for leveraging the force.com migration tool
* [Java JDK] is required for ant to run
* [Force.com Migration Tool] is an ant-based tool to access Salesforce's metadata API
* [Force.com CLI] is a CLI developed by Salesforce for accessing Salesforce
* [Salesforce Data Loader] is Salesforce's official data loading application

[Ant]: http://ant.apache.org/
[Java JDK]: http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html
[Force.com Migration Tool]: https://developer.salesforce.com/docs/atlas.en-us.daas.meta/daas/meta_development.htm
[Force.com CLI]: https://github.com/heroku/force
[Salesforce Data Loader]: https://developer.salesforce.com/page/Data_Loader

IDE:
* [Sublime Text] for coding
* [MavensMate] as our IDE to interface Sublime Text with Salesforce

[Sublime Text]: https://www.sublimetext.com/
[Mavensmate]: http://mavensmate.com/

If you choose to allow this script to configure your Sublime Application, you will receieve the
following plugins:
* [Package Control] For managing Sublime packages
* [Apex Snippets] for Apex Code snippets
* [DocBlockr] for code comments
* [GitGutter] for git diff capabilities in Sublime
* [Material Theme] as a default Sublime theme
* [MavensMate] to interact with the Mavensmate app
* [SublimeGit] git integration with Sublime

[Package Control]: https://packagecontrol.io/
[Apex Snippets]: https://packagecontrol.io/packages/Apex%20Snippets
[DocBlockr]: https://packagecontrol.io/packages/DocBlockr
[GitGutter]: https://packagecontrol.io/packages/GitGutter
[Material Theme]: https://packagecontrol.io/packages/Material%20Theme
[MavensMate]: https://packagecontrol.io/packages/MavensMate
[SublimeGit]: https://packagecontrol.io/packages/SublimeGit

Utilities:
* [Source Tree] as a GUI for git
* [Google Chrome] as a web browser

[Source Tree]: https://www.sourcetreeapp.com/
[Google Chrome]: https://www.google.com/chrome/

It should take less than 15 minutes to install (depends on your machine).

Contributing
------------

Fork, modify, and make a pull request.

License
-------
It is free software that has been forked from https://github.com/thoughtbot/laptop,
and may be redistributed under the terms specified in the [LICENSE] file.

[LICENSE]: LICENSE
