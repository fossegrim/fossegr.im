---
categories: [emacs, exploring-emacs]
layout: post
title: "Exploring Emacs Ⅰ: What Is Emacs and Why Should You Use It?"
---

> People talk about getting used to a new editor, but over time, it is precisely the opposite that should happen - the editor should get used to us. - Vivek Haldar

This series of posts will be about Emacs. I will be teaching and configuring it, starting from a blank slate and an empty configuration, all the way up to a usable and comfortable state. No prerequisite Emacs knowledge is required. The series is for beginner and intermediate Emacsers alike. If you already know Emacs well it is worth skipping a few chapters ahead.

Everything in this series will be tested on Linux and macOS although figuring it out on the saner of BSDs should also be possible. If you are using Windows I suggest running Emacs inside of a Linux virtual machine.

## What is Emacs?
Emacs is often referred to as a text editor although in reality it is much more than that. At its core Emacs is an integrated and programmable computing environment for running text oriented Emacs Lisp tools. These tools range from simple text editors, IDEs, IRC clients[^1], email clients[^2], life organizers[^3], terminal emulators[^4], version control interfaces[^5], [RSS readers]({% post_url 2020-06-09-rss-or-how-to-use-the-internet-without-letting-it-use-you%})[^6] and anything else you can think of. If you are dedicated enough you can even run a web browser inside Emacs. Emacs can also display images although that is not its main purpose.

## Why Should You Use it?
In my opinion there are four main properties that make Emacs a great program. Those are its keyboard control, consistency, hackability / extensibility and interoperability.

In Emacs everything can be done with keyboard commands. Once these become muscle memory, they have the potential of being much more efficient than doing the same with the mouse.

In Emacs all your tools generally have a consistent user interface and keybindings. Whereas you can achieve a similar experience without Emacs, that means having to manage separate configurations for all of your programs, which quickly becomes tedious and messy. Even then the consistency you get is subpar compared to that of Emacs.

Emacs is built to be extended and hacked. In Emacs there are thousands of easily installable packages from the Elpa and Melpa repositories. Extending it yourself is also simple.

There are built in tools to lookup the definition, docstring and value for every function and variable in Emacs. Emacs hackers share a strong documentation culture therefore *all* interesting functions have docstrings. If you ever wonder how something in Emacs works, finding out is simple.

Lastly interoperability. Emacs tools interact seamlessly with each other. This is expressed very well in this saying.

> Emacs provides functionality without applications. Rather than separate applications, functionality is all integrated into your Emacs instance. Amazingly, this works. Ever wanted to use the same snippet tool for writing C++ classes as well as emails?

In Emacs you can!

## Conclusion
All this may sound a little abstract at the moment, but as we progress through the series it will all be demonstrated along the way.

In the next chapter we will be installing Emacs and learn about basic usage.

If you have any feedback please [share](/contact/) it. I intend to make a YouTube series in parallel based on this so I greatly appreciate your suggestions.

Take Care

Olav

[^1]: Of the top of my mind I can think of ERC, circe and rcirc, but there are surely more. I use circe in my personal configuration.
[^2]: Rmail, Gnus and MH-E are shipped by default. There are many more in the repositories.
[^3]: The infamous org!
[^4]: Term and its variations are built in, but there is also a great package called vterm based on neovim's libvterm.
[^5]: Most notably Magit and vc. vc is version control system independent and shipped with Emacs whereas Magit is a third party package.
[^6]: I use elfeed. Which I briefly covered in my [RSS]({% post_url 2020-06-09-rss-or-how-to-use-the-internet-without-letting-it-use-you%}) article.
