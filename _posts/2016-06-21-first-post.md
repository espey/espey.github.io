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

3. Now you will have to build a windows vagrant box. Due to Microsofts EULA restrction, it is not currently possible to distribute Windows Vagrant boxes - even eval versions from publicly downloadable ISO images. This means we have to build the boxes ourselves. But, [Packer](https://www.packer.io/) makes this easier. But, you first will have to have Packer installed. To install packer, go to their homepage, press the [download link](https://www.packer.io/downloads.html) and find your operating system. This will give you a .zip file in your Downloads folder. Unzip the file and put the .exe in one of your $PATH locations (I put mine in `/usr/local`).Then, you should be able to run the `packer` command and an output similar to below should appear:

    <pre><code>usage: packer [--version] [--help] <command> [<args>] 
    Available commands are:
      build       build image(s) from template
      fix         fixes templates from old versions of packer
      inspect     see components of a template
      push        push a template and supporting files to a Packer build service
      validate    check that a template is valid
      version     Prints the Packer version

4.  Testing


