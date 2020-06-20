---
categories: [emacs, exploring-emacs]
layout: post
title: "Exploring Emacs Ⅱ: Installation and Basic Usage"
---

This chapter of Exploring Emacs will cover setting up Emacs and the basics of using it.

We will learn how to do text editing and use the help system along with the crucial concepts of the buffer, minibuffer, window, major-mode and minor-mode. 

## Installation
This section covers installing the Emacs application on macOS and Linux. I recommend reading this section even if you already have Emacs installed so as to verify that it is set up correctly.

## macOS
There are many ways of installing Emacs on macOS. The one we will be using is the emacs-plus package from Homebrew. If you aren't already familiar with Homebrew check out [https://brew.sh](https://brew.sh).

Provided that you have set up Homebrew all you need to do to install Emacs is run the following commands.

```sh
brew tap d12frosted/emacs-plus &&
brew install emacs-plus@27 --with-modern-icon-cg433n --with-xwidgets &&
ln -s /usr/local/opt/emacs-plus@27/Emacs.app /Applications
```

The `--with-modern-icon-cg433n` flag can be replace in case you want another icon. For a list of icons see [https://github.com/d12frosted/homebrew-emacs-plus#icons](https://github.com/d12frosted/homebrew-emacs-plus#icons).

## Linux
Installing Emacs on Linux is as simple as installing any other package. Simply install the Emacs package with your distribution's package manager. I can assure you that this package works correctly on Ubuntu. Although it will probably work as expected on other distributions too.

## Verification
To verify that you have installed the correct Emacs version, run `emacs --version` in your shell. Provided that the displayed version number is over 26 you are ready to move on.

![Correct Emacs Version](/assets/images/correct-emacs-version.png)

# Switching Ctrl placement
Emacs relies heavily on Ctrl. To avoid the infamous [Emacs Pinky](https://i.imgur.com/fX58Bw2.png) I recommend swapping the placement of Ctrl and Caps Lock on your computer.

## macOS
To do this on macOS open System Preferences and select the "Keyboard" option. Clicking on "Modifier Keys" will now bring up a prompt where you can switch the modifier keys as you wish.

![Modifier Keys Menu](/assets/images/modifier-keys.png)

You might have to restart your computer for this to take affect properly

## Linux
There is unfortunately no universal way of swapping Ctrl and Caps Lock on Linux. Most desktop environments have their own way of doing this and I am not delving into each one of them. You can find instructions for your desktop environment on the [Emacs Wiki](https://www.emacswiki.org/emacs/MovingTheCtrlKey).

## Launching Emacs
Emacs can be launched from the shell or as a desktop application. Both options do the same, but running it from the shell allows for the usage of launch flags. Some flags worth familiarizing yourself with are the "Q" and "nw" flags. The "Q" flag starts Emacs without loading your configuration and the "nw" flag runs Emacs in terminal mode. I do not suggest running Emacs in terminal mode as GUI Emacs is superior in a [variety of ways](https://blog.aaronbieber.com/2016/12/29/don-t-use-terminal-emacs.html). At the moment the GUI Emacs interface is ugly and cluttered, but we will clean it up in the next chapter. Just stick with it for now.
 
## The Tutorial
The best way to learn the very basics of Emacs is to do the tutorial. You can think of this as the Emacs equivalent of vimtutor. I choose to include this in my tutorial not out of laziness, but because it is an interactive tutorial which in my opinion is inherently superior to a non-interactive blog post.

It is crucial that you not only read the tutorial, but also interact with it as instructed. That is the only way to truly learn.

Before you read it you should know that Emacs uses different windowing terminology than what is common nowadays. What you normally call a window is called a frame in Emacs terms. The reason for this is that window has a special meaning in Emacs.

In Emacs a window is a section within your Emacs frame as illustrated by the following picture.
![Emacs windowing illustration](/assets/images/emacs-windowing-illustration.png)

To start the tutorial press `C-h t` inside Emacs. That is Ctrl and h at the same time followed by a lonely t. 

## Conclusion
To internalize the content of this tutorial I strongly suggest incorporating Emacs into your daily workflow. You do not have to start living entirely inside of Emacs quite yet, but you should gradually start doing more of your computing inside of it. Doing your one of text editing tasks with it is a good start for now.

In the next chapter of Exploring Emacs we will learn Emacs Lisp and start customizing our Emacs configuration.

If you found this interesting or have any questions regarding the article feel free to join my Discord server [fossegrim's club](https://discord.gg/Dzykafx) or [contact](/contact/) me otherwise! As always I appreciate your feedback!

Thanks for reading!

Take care

Olav
