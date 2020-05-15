Hello,

I set this page up because I thought that Github's interface is not that well suited to a resume. It's hard to distinguish one's own projects from contributions made to other projects. Here, I would like to highlight some of the examples you might be looking for, and give a little context to them.

I should note that while I've been a Node.js and Go developer by trade, Python is still my strong suit, and I'm a big fan of Haskell. You may find a disproportionate amount of Haskell among what I've done in my free time, which has a strong correlation with what ends up on Github. But, I've included some Python.

# Code Samples

## Open Source Contributions

### Etherpad (JavaScript)

I've done some work for the Etherpad project on a contract basis. I will point to a few particular pull requests:

#### [Fixing WebRTC Error Messages](https://github.com/ether/ep_webrtc/pull/36/)

This is for a WebRTC plugin that let document editors have an A/V chat. The error messages for making the connection were wrong. While investigating I realized that there were some rather jarring changes in the webrtc spec as far as error messages go. Errors that are thrown changed meanings over time. One error condition actually changed from throwing an Error to making the function `undefined`. This requires us to do ridiculous introspection to have a best guess as to what an error exactly means, in a way that works across all browsers we wish to support.

That said, understanding as I do now about adapter.js, I would probably have tried updating that instead of putting those changes in the Polyfill.

#### [Fix color picker bug](https://github.com/ether/etherpad-lite/pull/3730)

Fix a bug with the color picker for the user's representation in a collaborative document. The change itself is one line, but the test is a lot more.

#### [Fix clearing cookies in tests](https://github.com/ether/etherpad-lite/pull/3775)

While running the test suite, I found that cookies were not resetting properly, creating the possibility of false positives for passing tests. This change includes a fix for it, as well as a test for it (even though it is itself a test helper function).

#### README updates developer testing instructions for WebRTC [on localhost](https://github.com/ether/ep_webrtc/pull/32) and [with SSL](https://github.com/ether/ep_webrtc/pull/42/files)

A couple minor documentation examples, again on the WebRTC plugin. It was my first time working with WebRTC and there was some on-ramp time trying to sort out why certain errors were coming. I wanted to try to speed that part along for the next person.

## My Own Projects

### [Haskell-Synth](https://github.com/orblivion/Haskell-Synth)

An attempt to make a Sound/Music synthesizer, in Haskell. It generates a simple sequence of electronic music based on hard coded instructions. It really sold me on Haskell, as I made some really sophisticated refactors and the compiler kept me in check to an astounding degree.

### [Feed Getter (Haskell)](https://github.com/orblivion/feedGetter)

A Podcast downloader written in Haskell that takes advantage of Haskell's async paradigm. (No UI; I prefer to use my existing audio players)

### [Fee Fighters - Samurai Python Client](https://github.com/orblivion/samurai-client-python/tree/demo)

The initial version of the Python client for the Samurai api created by FeeFighters (now part of Groupon). I created this while working for Alltuition in 2011, where we were using FeeFighters to process payments. I should note that this is early in my Python days, and I've improved my style since then. (Though, you'll see I did a cleanup pass of this code in 2016).

### [Kiwix package for Sandstorm](https://github.com/orblivion/KiwixSandstorm)

This project is to package an application called [Kiwix](https://www.kiwix.org) for a platform called [Sandstorm](https://sandstorm.io). Neither Kiwix nor Sandstorm per se are my own work.

Kiwix makes it easy to have your own copy of Wikipedia and many other open data sites. However, as with any self-hosted web\* application, it requires a small amount of maintenance to set up and maintain. Sandstorm is a platform that greatly reduces maintenance of running self-hosted applications. Here it is [listed on the Sandstorm Marketplace](https://apps.sandstorm.io/app/5uh349d0kky2zp5whrh2znahn27gwha876xze3864n0fu9e5220h). Sandstorm is a very restrictive environment and requires some work to configure an application to work with it. Once it does, though, it has the benefits of simplicity of maintenance, security, and even some interoperability with other applications.

This is mostly a packaging/building exercise, and I helped Kiwix identify some [build errors](https://github.com/kiwix/kiwix-lib/issues/44) and even a [licensing problem](https://github.com/openzim/libzim/issues/30) along the way. It is also in part a development exercise, as it includes a custom uploader that played well with Sandstorm, though it was rather hacked together and is not the greatest example of my work as a developer per se. In particular, I needed to handle large files in a novel way as Sandstorm at the time did not support proper Range requests.

\* Kiwix also comes as a phone and desktop application

## Random Exercises/Samples
  * **[Python](https://github.com/orblivion/hellolabs_word_test)**:
  * **[Erlang (without OTP)](https://github.com/orblivion/erlang_chat_exercise)**
  * **[Haskell](https://github.com/orblivion/random-chain)**
