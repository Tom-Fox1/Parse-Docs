# Parse Docs

> These new docs are far from finished the current ones can be found [here](http://parseplatform.org). Any help in completing these docs is much appreciated - see the [discussion about these new docs](https://community.parseplatform.org/t/consolidate-documentation/149) and the [migration guide](migrationGuide.md).

[![Website](https://img.shields.io/website/https/tom-fox1.github.io/Parse-Docs.svg?down_color=red&up_message=live)](https://tom-fox1.github.io/Parse-Docs)
[![Build Status](https://travis-ci.org/Tom-Fox1/Parse-Docs.svg?branch=master)](https://travis-ci.org/Tom-Fox1/Parse-Docs)
[![Join The Conversation](https://img.shields.io/discourse/https/community.parseplatform.org/topics.svg)](https://community.parseplatform.org/c/parse-server)
[![Backers on Open Collective](https://opencollective.com/parse-server/backers/badge.svg)][open-collective-link]
[![Sponsors on Open Collective](https://opencollective.com/parse-server/sponsors/badge.svg)][open-collective-link]
[![License][license-svg]][license-link]
[![Twitter Follow](https://img.shields.io/twitter/follow/ParsePlatform.svg?label=Follow%20us%20on%20Twitter&style=social)](https://twitter.com/intent/follow?screen_name=ParsePlatform)

These are the markdown sources for all of the [Parse SDK guides](https://parse-community.github.io/#sdks), the Cloud Code guide and the Parse Server guide. The content for the guides is stored in this repo, these docs have been created with [Slate](https://github.com/lord/slate) which then generates a static site that is hosted on GitHub Pages.

Getting Started with the Parse Docs
------------------------------

### Prerequisites

You're going to need:

 - **Linux or macOS** — Windows may work, but is unsupported.
 - **Ruby, version 2.3.1 or newer**
 - **Bundler** — If Ruby is already installed, but the `bundle` command doesn't work, just run `gem install bundler` in a terminal.

### Getting Set Up

1. Fork this repository on GitHub.
2. Clone *your forked repository* (not our original one) to your hard drive with `git clone https://github.com/YOURUSERNAME/Parse-Docs.git`
3. `cd Parse-Docs`
4. Initialize and start the Parse Docs. You can either do this locally, or with Vagrant:

```shell
# either run this to run locally
bundle install
bundle exec middleman server

# OR run this to run with vagrant
vagrant up
```

You can now see the docs at http://localhost:4567. Whoa! That was fast!

Now that the Parse Docs are all set up on your machine, you'll probably want to learn more about [editing Slate markdown](https://github.com/lord/slate/wiki/Markdown-Syntax).

Questions? Need Help? Found a bug?
--------------------

Found a bug with upstream Slate? Go ahead and [submit an issue](https://github.com/lord/slate/issues). And, of course, feel free to submit pull requests with bug fixes or changes to the `dev` branch.

[license-svg]: https://img.shields.io/badge/license-BSD-lightgrey.svg
[license-link]: LICENSE
[open-collective-link]: https://opencollective.com/parse-server
