moodle-lifecycletrigger_customfieldsemester
===========================================

[![Moodle Plugin CI](https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester/workflows/Moodle%20Plugin%20CI/badge.svg?branch=master)](https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester/actions?query=workflow%3A%22Moodle+Plugin+CI%22+branch%3Amaster)

Moodle trigger subplugin for the Moodle admin tool "Course Life Cycle" which triggers based on values of a custom course field of type "semester".


Requirements
------------

This plugin requires Moodle 3.9+

Additionally, this plugin requires the Moodle plugin tool_lifecycle which is published on https://github.com/learnweb/moodle-tool_lifecycle.
Furthermore, it requires the Moodle plugin customfield_semester which is published on https://github.com/learnweb/moodle-customfield_semester.


Installation
------------

Install the plugin like any other plugin to folder
/admin/tool/lifecycle/trigger/customfieldsemester

See http://docs.moodle.org/en/Installing_plugins for details on installing Moodle plugins


Usage & Settings
----------------

After installing the plugin, it does not do anything to Moodle yet.

To configure the trigger and its behaviour, please visit:
Site administration -> Plugins -> Admin tools -> Life Cycle -> Workflow settings and add a new workflow there.

Within this workflow, please add a new trigger instance of type "Customfield semester trigger".

Within the trigger configuration, you have two specific settings to define:

### 1. Custom field

With this setting, you define the (pre-existing) custom field which holds the term of a course. The value of this field will be the basis of this trigger.

### 2. Trigger x months after term start

With this setting, you define the delay until a process is started.

The trigger will take the term of a course, get the start month of the term, add the configured amount of months as delay and check if this delay period has already passed. If yes, the trigger will be invoked.

Courses which have the 'term-independent' value in the custom course field will never be triggered.


Theme support
-------------

This plugin acts behind the scenes, therefore it should work with all Moodle themes.
This plugin is developed and tested on Moodle Core's Boost theme.
It should also work with Boost child themes, including Moodle Core's Classic theme. However, we can't support any other theme than Boost.


Plugin repositories
-------------------

This plugin is not published in the Moodle plugins repository yet.

The latest development version can be found on Github:
https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester


Bug and problem reports / Support requests
------------------------------------------

This plugin is carefully developed and thoroughly tested, but bugs and problems can always appear.

Please report bugs and problems on Github:
https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester/issues

We will do our best to solve your problems, but please note that due to limited resources we can't always provide per-case support.


Feature proposals
-----------------

Due to limited resources, the functionality of this plugin is primarily implemented for our own local needs and published as-is to the community. We are aware that members of the community will have other needs and would love to see them solved by this plugin.

Please issue feature proposals on Github:
https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester/issues

Please create pull requests on Github:
https://github.com/hsh-elc/moodle-lifecycletrigger_customfieldsemester/pulls

We are always interested to read about your feature proposals or even get a pull request from you, but please accept that we can handle your issues only as feature _proposals_ and not as feature _requests_.


Moodle release support
----------------------

This plugin is only maintained for the most recent major release of Moodle.

Apart from this maintained release, previous versions of this plugin which work in legacy major releases of Moodle are still available as tagged release commits on Github.

There may be several weeks after a new major release of Moodle has been published until we can do a compatibility check and fix problems if necessary. If you encounter problems with a new major release of Moodle - or can confirm that this plugin still works with a new major release - please let us know on Github.

If you are running a legacy version of Moodle, but want or need to run the latest version of this plugin, you can get the latest version of the plugin, remove the line starting with $plugin->requires from version.php and use this latest plugin version then on your legacy Moodle. However, please note that you will run this setup completely at your own risk. We can't support this approach in any way and there is an undeniable risk for erratic behavior.


Translating this plugin
-----------------------

This plugin does not contain any strings which are visible to a Moodle student / teacher and it can't be translated on AMOS as it is not published in the Moodle plugins repository. In our point of view, translating this plugin is not necessary.


Right-to-left support
---------------------

This plugin has not been tested with Moodle's support for right-to-left (RTL) languages.
If you want to use this plugin with a RTL language and it doesn't work as-is, you are free to send us a pull request on Github with modifications.


PHP7 Support
------------

Since Moodle 3.4 core, PHP7 is mandatory. We are developing and testing this plugin for PHP7 only.


Copyright
---------

Alexander Bias

on behalf of

Hochschule Hannover
Servicezentrum Lehre E-Learning (elc)
