---
layout: post
title: My website
subtitle: or how to get yours
---

Here we are, willing for an online visibility. How to set that up quickly when you start from scratch ? Remember those html courses ?

Yeah me neither. But fortunately for us [github](https://github.com/) made it easier than ever!

What's [github](https://github.com/) ? Alright, we'll start from scratch but you'll only get more readings - of course if you are familiar with all that stuff, well scroll-scroll.

Here is [github's wikipedia page](https://en.wikipedia.org/wiki/GitHub), in short it's a tool that let you keep tracks of your work progress. Like hitting that infamous `save` button, a little less simple but a lot more powerful. A lot more powerful because you can keep tracks of the whole history of whatever it is that you are working on (article, book, code, maybe your country next constitution). And you can do that in a clear, transparent and collaborative way if you want so.

To be fair [github](https://github.com/) is only (so to speak) a layer for [git](https://git-scm.com/), but I'm fairly sure that github brought that awesomeness to the mass.

You've notice right ? That the last occurrence of the word [github](https://en.wikipedia.org/wiki/GitHub) wasn't a link ? Well here comes [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). markdown is a rather easy way to write content for your website. You can learn more about markdown from [this tutorial](http://markdowntutorial.com/) and guess what, fom [this tutorial in french](https://openclassrooms.com/courses/redigez-en-markdown).

But first lets set up all the necessary stuff to get started, shall we ?

**Github**

1.  First of all, let's [register on github](https://github.com/join) if you don't have an account yet.

2.  Then create a github repo (project) that will hold your website. To do so hit the tiny cross (+) in the top-right of the github webpage and select `new repository`. For github to be able to figure out that this particular repo is your website you need to give it a special name in the form : **[your-user-name].github.io**.

**Jekyll**

<!-- <img src="/images/fulls/02.jpg" class="fit image"> -->

1.  [Jekyll](https://jekyllrb.com/) is basically the guy whose going to convert your plain [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) text files into webpages. There is some documentation and everything to get started on [jekyll](https://jekyllrb.com/) website but we are lazy so we are going to use a website template ! Yes there are nice people out-there who wrote website template such that you don't have to worry about all the setup and configuration and blablabla. If you are a complete beginner I invite you to pass the scary command below and continue directly with the second point.

    Let's have a quick look at the second bullet point, pick a template, and clone it. You may pick a random one for th purpose of testing.

    Now that I have a local copy of a marvelous template, of course the [Jekyll Quick start guide](https://jekyllrb.com/docs/quickstart/) wasn't enough to get started in 5min (my setup Ubuntu 14.04 64-bit).
    First of all my version of [Ruby](https://www.ruby-lang.org/en/) was outdated. Jekyll seems to require version 2 at least.

    ```terminal
    $ ruby -v
    ruby way-to-oldp643 [x86_64-linux-gnu]
    ```
    How come ? That's the last version from Ubuntu repo :'(  
    Alright let's install it from another repo.

    ```terminal
    $ sudo apt-add-repository ppa:brightbox/ruby-ng
    $ sudo apt-get update

    $ sudo apt-get install ruby2.2-dev
    ```
    Now we can install jekyll & bundle.  
    And try to build the website.

    ```terminal
    $ sudo gem install jekyll bundler

    $ jekyll build
    Your bundle is locked to json (1.8.3), but that version could not be found in any of the sources  
    - or else -  
    but your Gemfile requires colorator 0.1 etc etc.
    ```
    Yeah apparently we messed up big time. The ruby  version we just installed is in conflict with the system's ruby version and jekyll doesn't figure out all the deps by itself.  
    Fortunately bundle does. So we just going to execute jekyll through bundle rather than fixing those deps. Laziness, I told you.

    ```terminal
    $ bundle install
    $ bundle exec jekyll build
    ```
    Since everything went fine this time (I hope that it did for you as well, otherwise, google is your friend) we can have a look at our website locally before letting it goes to the online world.

    ```terminal
    $ bundle exec jekyll serve
    ```

    The above command launch a local server that will let you access your website from your favorite web browser at the address `http://localhost:4000/`.

2.  So, now is the time to flatter this tiny designer in yourself and spend ours (or not) choosing a template. Keep in mind that the most good looking one is probably not the easiest one to deal with. A good place to start is on the [jekyll template page](http://jekyll.tips/templates/). If most of them follow the same scheme for configuring, editing, tweaking your own personal site, they still have subtle differences and that why I encourage you to read their installation/configuration explanations. Remember ? Laziness.

In case you are wondering which is the template of this very website ? [beautiful jerkyll](https://github.com/daattali/beautiful-jekyll)

From there on I basically invite you to read the "**Build your website in 3 steps**" tutorial of beautiful jerkyll. [Here it is](https://github.com/daattali/beautiful-jekyll#build-your-website-in-3-steps).


**Some other tips**

Get a github button that you can copy/pasta ! [github button](https://buttons.github.io/).

<!-- Place this tag where you want the button to render. -->
<a class="github-button" href="https://github.com/artivis" data-style="mega" data-count-href="/artivis/followers" data-count-api="/users/artivis#followers" data-count-aria-label="# followers on GitHub" aria-label="Follow @artivis on GitHub">Follow @artivis</a>
