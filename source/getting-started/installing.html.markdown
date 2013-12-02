---
title: "Installing Test Kitchen"
next:
  text: "Getting Help"
  url: "getting-help"
---

Okay let's get down to it, shall we? Test Kitchen is packaged and delivered to you as a [RubyGem](http://guides.rubygems.org/what-is-a-gem/). If you've used Chef, Puppet, or Rails before then working with Gems shouldn't present a huge challenge. If all this Ruby "stuff" is new, then don't dispair--we're going to steer clear of a lot of Ruby-looking code.

To follow this guide there is some software that we will need in order for Test Kitchen to do its thing:

* A Ruby distribution - version 1.9 and higher
* Git - oh yes, we're going to be commiting code
* Vagrant - a great tool to help manage development virtual machines
* VirtualBox - a virtualization tool that let's you run virtual machines locally

I know, it sounds like a lot of work but don't depair. We're going to follow the [Workstation Setup](https://learnchef.opscode.com/quickstart/workstation-setup/) instructions from the [#learnchef](https://learnchef.opscode.com/) website. Take a few minutes to get your software setup and if you run into any issues there should be some smart and capable people in the [#learnchef](http://webchat.freenode.net/?channel=learnchef) IRC chatroom to get you back on track.


> **All done? Great! Open a terminal window and let's get started.**

Installing Test Kitchen from RubyGems goes like this:

~~~
$ gem install test-kitchen
Fetching: timers-1.1.0.gem (100%)
Successfully installed timers-1.1.0
Fetching: celluloid-0.15.2.gem (100%)
Successfully installed celluloid-0.15.2
Fetching: thor-0.18.1.gem (100%)
Successfully installed thor-0.18.1
Fetching: coderay-1.0.9.gem (100%)
Successfully installed coderay-1.0.9
Fetching: slop-3.4.6.gem (100%)
Successfully installed slop-3.4.6
Fetching: method_source-0.8.2.gem (100%)
Successfully installed method_source-0.8.2
Fetching: pry-0.9.12.2.gem (100%)
Successfully installed pry-0.9.12.2
Fetching: net-ssh-2.7.0.gem (100%)
Successfully installed net-ssh-2.7.0
Fetching: net-scp-1.1.2.gem (100%)
Successfully installed net-scp-1.1.2
Fetching: mixlib-shellout-1.2.0.gem (100%)
Successfully installed mixlib-shellout-1.2.0
Fetching: safe_yaml-0.9.7.gem (100%)
Successfully installed safe_yaml-0.9.7
Fetching: test-kitchen-1.0.0.beta.3.gem (100%)
Successfully installed test-kitchen-1.0.0.beta.3
12 gems installed
~~~

Now if the version of Test Kitchen is important to you, then you can add a `-v <version_string>` to the end of the `gem install` command. Alternatively if you prefer living on the edge, adding a `--pre` to the install command will give you the latest alpha/beta/release candiate release. Note that these releases may not be as stable but your courage and feedback is greatly appreciated.


|| *Pro-Tip*
|| If you are familiar with and use <a href="http://bundler.io/">Bundler</a> then you can safely add `gem "test-kitchen"` to your project's *Gemfile*. Just don't forget to `bundle install`.


Now let's verify that Test Kitchen is installed. To save on typing, the tool's main command is `kitchen`. So to get the currently installed version we type:

~~~
$ kitchen version
Test Kitchen version 1.0.0.beta.3
~~~
