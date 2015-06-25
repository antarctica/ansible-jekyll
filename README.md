# Jeykll (`jekyll`)

**Part of the BAS Ansible Role Collection (BARC)**

Installs the Jekyll static site generator and optional plugins/extensions

## Overview

* Installs the Jekyll gem
* Optionally, installs the Rouge syntax highlighting gem, this is enabled by default

## Availability

This role is designed for internal use but if useful can be shared publicly.

## Usage

### Requirements

#### BAS Ansible Role Collection (BARC)

* `core`

#### Ansible Galaxy

* `rvm_io.rvm1-ruby`

### Variables

* `jeykll_jekyll_version`
    * Version of the Jekyll gem to install
    * This variable **MUST** be a valid gem version, as determined by [rubygems](https://rubygems.org/gems/jekyll/versions).
    * This variable **SHOULD** be set to the latest stable version of the gem, and will be updated whenever this role is modified.
    * Default: "2.5.3"
* `jeykll_gem_path`
    * Path to the `gem` executable used to install ruby gems
    * The default value for this variable is a conventional default, it **SHOULD NOT** therefore be changed.
    * Default: "/usr/local/rvm/bin/rvm all do gem"
* `jeykll_enable_feature_install_rouge`
    * If "true", the rouge gem will be installed to provide syntax highlighting support within Jekyll 
    * This is a binary variable and **MUST** be set to either "true" or "false" (without quotes).
    * Default: "true"
* `jeykll_rouge_version`
    * Where the rouge gem is installed, the version of the gem to install
    * This variable **MUST** be a valid gem version, as determined by [rubygems](https://rubygems.org/gems/rouge/versions).
    * This variable **SHOULD** be set to the latest stable version of the gem, and will be updated whenever this role is modified.
    * Default: "1.9.0"

## Contributing

This project welcomes contributions, see `CONTRIBUTING` for our general policy.

## Developing

### Committing changes

The [Git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow/) workflow is used to manage development of this package.

Discrete changes should be made within *feature* branches, created from and merged back into *develop* (where small one-line changes may be made directly).

When ready to release a set of features/changes create a *release* branch from *develop*, update documentation as required and merge into *master* with a tagged, [semantic version](http://semver.org/) (e.g. `v1.2.3`).

After releases the *master* branch should be merged with *develop* to restart the process. High impact bugs can be addressed in *hotfix* branches, created from and merged into *master* directly (and then into *develop*).

### Issue tracking

Issues, bugs, improvements, questions, suggestions and other tasks related to this package are managed through the BAS Web & Applications Team Jira project ([BASWEB](https://jira.ceh.ac.uk/browse/BASWEB)).

## License

Copyright 2015 NERC BAS. Licensed under the MIT license, see `LICENSE` for details.
