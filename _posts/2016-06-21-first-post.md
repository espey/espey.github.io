---
layout: post
title: "Espey, Techy Blogy has been created!"
date: 2016-06-21
---

Yay! I finally have a blog that works! I'm not quite sure the format of this blog quite yet. Or, what I will be posting. But today, I wanted to learn more about Active Directory for Windows. I also think it would be nifty to set up Active Directory via a Chef Script. So, these next few blog posts will be surrounding those two concepts. 

## Using Kitchen::Vagrant with Windows 2012
1. The [kitchen-vagrant 0.17.0](https://github.com/test-kitchen/kitchen-vagrant/releases/tag/v0.17.0) release comes with the ability to spin up Windows instances. So, be sure that `gem list kitchen-vagrant` shows a version equal to or greater than 0.17.0. You may need to run `gem install kitchen-vagrant`. 

2. Next, you need to make the WinRM host and port detection logic work - so, you will have to install a vagrant plugin called `vagrant-winrm`. This is a vagrant plugin and will be available to any future Vagrant projects on your workstation. To install run this:

  ```
  vagrant plugin install vagrant-winrm
  ```
3. 


