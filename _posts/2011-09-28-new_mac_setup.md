---
published: false
layout: post
title: What to install on your new - old - Mac
categories:
- other
---

### A quick list of the first installs I perform on Mac OSX 10.5 that make using the Mac even more awesome.

### (In roughly the order in which I install them)

[Xcode](http://developer.apple.com)
-----------------------------------

This comes on the install disk, but I always try to get the latest from [developer.apple.com](http://developer.apple.com) . Even if you are not planning on developing Cococa applications, you still want Xcode because it installs c / c++ compilers required for getting some Unix software up and going on the Mac.

Apple wants you to either get Xcode from the App store or sign up for their $100 / year developer programs. But, you can get Xcode 3 from Apple for free by signing up as a developer here:

<http://developer.apple.com/programs/register/>

For Mac OSX 10.5, you want Xcode 3.1.4 (the latest version of Xcode that will work on this OS.)
It is kind of tricky to find. You can [go to the download page](http://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wo/5.1.17.2.1.3.3.1.0.1.1.0.3.3.3.3.1) and search for Xcode 3.1.4 in the “Developers Tools” section of the site.

[Homebrew](https://github.com/mxcl/homebrew)
--------------------------------------------

Becoming the defacto standard for easily installing Unix tools on the Mac. Homebrew solves the same problems as apt-get or yum in Linux land, however it is made for the Mac.

There are other tools (Macports & Fink) that used to be the mainstays for installing Unix software on the Mac, however homebrew is becoming the popular choice in part because it is much less opaque than other tools to use. The tool and all its packages are managed on [github](http://github.com) . The package installers are really just ruby scripts, which makes it easy to add a new package to the mix. And its really quite easy to use:

{% highlight bash %}
brew install git
{% endhighlight %}

**Note:** Easy installation of tools assumes a certain file ownership on the system. If you have problems installing packages related to permissions, try changing the owner of /usr/local/ to yourself:

{% highlight bash %}
sudo chmod -R [USERNAME] /usr/local
{% endhighlight %}

[RVM](https://rvm.beginrescueend.com/)
--------------------------------------

The [ruby package manager](https://rvm.beginrescueend.com/) makes it easy to use ruby on Unix systems. It manages multiple versions of ruby and the gems associated with them, so you don’t have to worry about incompatible setups when using different versions.

**Note:** I usually have to use the `-k` switch for the install process to get things working as detailed on the [install page](https://rvm.beginrescueend.com/rvm/install/) .

{% highlight bash %}
bash < <(curl -sk https://rvm.beginrescueend.com/install/rvm)
{% endhighlight %}

Once installed, I always get ruby 1.9 going on my system

{% highlight bash %}
rvm list known
rvm install 1.9.2
rvm use 1.9.2 --default
{% endhighlight %}

[Quicksilver](http://www.blacktree.com/)
----------------------------------------

Quicksilver is usually the first thing I get setup on my Mac. Without it, I feel lost and alone. With it, I’m unstoppable.

Quicksilver is many things to many people. In its simplest form you can use it as a quick application launcher. With a bit more experience, it becomes a file browser. Eventually, it is the main interaction point you have with your Mac. Forget the mouse, use Quicksilver!

It can be a bit troublesome to get going - but its worth it. I’ve had good luck so far with using [version B58](https://github.com/downloads/quicksilver/Quicksilver/Quicksilver-b58-3841.tar.gz) with 10.5.

Recently, there has been some movement in the Quicksilver world - a [new website](http://qsapp.com/index.php) and a [new release](http://qsapp.com/download.php) (along with new developers). I’ve yet to move up to B60…

[MacFUSE](http://code.google.com/p/macfuse/) & [Macfusion](http://macfusionapp.org/)
------------------------------------------------------------------------------------

There are times when I want to mount a SSH login as if it were a filesystem. Sometimes, its a remote machine. Sometimes, its a machine I can already mount, but I need to mount it as a different user.

[Macfusion](http://macfusionapp.org/) lets me do this easily, and [MacFUSE](http://code.google.com/p/macfuse/) is the glue that Macfusion uses to get that done.

I’m not sure how difficult this is to get set-up. I didn’t really have any problems on 10.5 - but I think 10.6 users might have issues. First download and install MacFUSE. Then grab Macfusion as the frontend. I’m using Macfusion 2.0.3 and MacFUSE 2.0.3 as well.

### Done with the hard part, now for some easy application installs

[R](http://cran.r-project.org/bin/macosx/) & [RStudio](http://www.rstudio.org/)
-------------------------------------------------------------------------------

In the bioinformatic world, you better have a good R setup. I think RStudio is the best I’ve seen - even if you use command line R for the most part, RStudio is worth having on your system. First get the latest version of [R](http://cran.r-project.org/bin/macosx/) on your mac, then grab the [RStudio Desktop App](http://www.rstudio.org/download/) and use that as your R frontend.

[Chrome](http://www.google.com/chrome/intl/en/make/download-mac.html) & [Firefox](http://www.mozilla.com/)
----------------------------------------------------------------------------------------------------------

Safari is a fine browser, I just like using Chrome better for the time being. Firefox is great to have too for plugins and for when Chrome and a website don’t play nicely.

[MacVim](http://code.google.com/p/macvim/)
------------------------------------------

Vim is Vim is Vim - until you start using [MacVim](http://code.google.com/p/macvim/) .
Try it out, and have a look at [my dotfiles](https://github.com/vlandham/dotfiles) to see how to perfect the MacVim experience.

[TextWrangler](http://www.barebones.com/products/textwrangler/)
---------------------------------------------------------------

Sometimes you don’t want to deal with Vim - even MacVim. There are other times when a more ‘normal’ text editor makes sense. These are the times to use [TextWrangler](http://www.barebones.com/products/textwrangler/) .

It handles large files well, it does syntax highlighting, it has text manipulation tools built in, and its free. There is nothing not to like.

[Skim](http://skim-app.sourceforge.net/)
----------------------------------------

The best darn pdf reader ever, ever. No competition anywhere. Does highlighting / notes. Easy navigation. And has a [great motto](http://skim-app.sourceforge.net/) .

[GitX](http://gitx.frim.nl/)
----------------------------

I don’t always use a Git GUI, but when I do, I prefer [GitX](http://gitx.frim.nl/)

[Adium](http://adium.im/)
-------------------------

Adium is just a nice instant messaging client. You already have iChat built in, but I typically use Adium because I like its interface a bit better.

[MacTex](http://www.tug.org/mactex/)
------------------------------------

For when you decide you want to try Latex one more time, [MacTex](http://www.tug.org/mactex/) is your best bet. Its large and slow to download. But easy enough to install. I don’t use most of the programs directly (though [LaTeXIT](http://www.chachatelier.fr/latexit/latexit-home.php?lang=en) is included, which is particularly nice), but it gives you all the command line tools needed to get going with Latex fast (after the download, which does take an eternity).

### Other programs you will want eventually

-   [Eclipse](http://www.eclipse.org/downloads/packages/eclipse-ide-java-developers/indigor) - because sooner or later you are going to want to write Java.
-   [The Unarchiver](http://wakaba.c3.cx/s/apps/unarchiver.html) - Faster than the built in extraction tool and supports more formats.
-   [Cyberduck](http://cyberduck.ch/) - Ftp/sftp client. Be ready when you need to deal with ftp, cause it’ll happen.
-   [Dropbox](http://www.dropbox.com/) - Everyone should use Dropbox.
-   [Mendeley](http://www.mendeley.com/) - Paper tracking. I like [Papers](http://www.mekentosj.com/papers/) , but you can’t beat free and cross-platform.
-   [Inkscape](http://inkscape.org/) - Nice free vector graphics editor to have.
-   [Virtual Box](http://www.virtualbox.org/) - VM is going to be huge! Oh wait, it already is.
-   [Growl](http://growl.info/) - Everyone uses Growl for notifications. Don’t miss out on all the action.
