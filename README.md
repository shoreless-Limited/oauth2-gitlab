# The Bug Genie GitLab OAuth2 authentication module

## Description

This is an authentication  module for [The Bug Genie](https://github.com/thebuggenie/thebuggenie)
issue tracker. It allows authenticating The Bug Genie users against GitLab as OAuth2 provider.  


## Requirements

  * A running [The Bug Genie](https://github.com/thebuggenie/thebuggenie) installation, v4.2+
  * A running [GitLab](https://about.gitlab.com/) installation, v8.17+
  * PHP 5.6+
  * [Composer](https://getcomposer.org/doc/00-intro.md)


## Installation

REMARKS: Replace `thebuggenie` within the examples with your path to your The Bug Genie installation.  


### 1: The Bug Genie Module Installation

Clone this repository either straight into a folder under `thebuggenie/modules/oauth2_gitlab`,
download the sources and extract them to `thebuggenie/modules/oauth2_gitlab`, or symlink the
sources to the same folder (IMPORTANT: The folder name under thebuggenie/modules MUST be
`oauth2_gitlab`, as The Bug Genie requires the module folder to match the module name):

<pre>
cd thebuggenie/modules
git clone git@github.com:shoreless-ltd/tbg-oauth2-gitlab.git oauth2_gitlab
</pre>


### 2: Install Composer Dependencies

This module uses the [omines/oauth2-gitlab](https://packagist.org/packages/omines/oauth2-gitlab)
composer package, which must be installed after you installed the module to The Bug Genie.  

Navigate to the `thebuggenie/modules/oauth2_gitlab` folder and install the composer dependencies:  

<pre>
cd thebuggenie/modules/oauth2_gitlab
composer install
</pre>


### 3: Activate the Module

You can now enable the module from the configuration section in The Bug Genie.


### 4: Configure GitLab / The Bug Genie

After activating the module, head over to the GitLab OAuth2 settings in The Bug Genie to setup the
application key and secret, as well as the GitLab instance you like to authenticate against.

To generate an application key and secret, follow the instructions under
[Adding an application through the profile](https://docs.gitlab.com/ce/integration/oauth_provider.html#adding-an-application-through-the-profile)
within the GitLab docs. (Depending on the GitLab version you are using, the GUI might slightly
differ from the given screenshots of this tutorial.)


## Reporting issues

If you find any issues, please report them in the issue tracker:
https://github.com/shoreless-ltd/tbg-oauth2-gitlab/issues