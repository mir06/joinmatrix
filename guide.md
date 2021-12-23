---
title: Guide
layout: page-two-col
nav: true
parent: guide
permalink: guide/
---

Welcome! This website aims to be a beginner-friendly guide to Matrix (sometimes mistakenly known as Element). Without further due, let's begin:

## Why Matrix?

Matrix is the long-awaited middleground between one-to-one messaging platforms (Facebook Messenger, WhatsApp, iMessages, SMS...) and social/collaborative messaging platforms (Discord, Slack, Telegram...): It offers an appropriate degree of privacy while allowing you to socialize/collaborate with others. Generally, the merits that make Matrix stand out from others can be boiled down to two categories:

* **Freedom.** You get to choose how you use the platform and how your data is treated.
  * Conversations can be end-to-end encrypted[^1]. This is enabled by default for direct and group messages[^2].
  * Automatic collection of data is minimized: No contact syncing[^3], no "are you human?" checks beyond registration, phone numbers are optional, even email addresses are optional (on select homeservers)!
  * You can host your own server, or you can join [an existing public homeserver](../servers) that suits you. Either way, your access to the Matrix federation is the same[^4]!
  * Bridges allow you to chat with users on other platforms, minimizing the social cost of moving to Matrix!
* **Trust.** You get to actually trust the software you use.
  * Matrix is an open protocol, and most of its [clients](#what-clients-should-i-use) and servers[^5] are both open source, which you may contribute to!
  * You are welcomed to improve Matrix by creating new clients and/or server implementations, or by [reviewing or submitting](https://spec.matrix.org/unstable/proposals/) proposals. You can shape your platform towards a better direction!
  * Matrix is of European origin, which breaks the American hegemony on chat platforms, since the United States is not exactly known for respecting data privacy or best practices.
  * Matrix is backed by the public sector, most notably by the Germans ([healthcare](https://matrix.org/blog/2021/07/21/germanys-national-healthcare-system-adopts-matrix), [army](https://element.io/case-studies/bundeswehr), [universities](https://doc.matrix.tu-dresden.de/en/why/)) as well as [the French](https://element.io/case-studies/tchap).

Some other reasons that may be attractive:

* Since Matrix is an open protocol, it is extensible and can be used for purposes beyond just chatting. For example: [help desk](https://www.safesupport.chat/), [social media](https://minestrix.henri2h.fr/), real-time collaboration...
* Matrix's federated nature makes the platform difficult, if not impossible, for a "big tech" to acquire, or for a regime to censor.

And of course, Matrix has the features that everyone else has: Cross-platform, real-time, etc. But that's not the point. Matrix shows that it is **possible** to have a decent chat platform that actually **respects you**.

## Get Started

Ready to try Matrix? Here we go:

### Set up own homeserver, or join an existing homeserver?

<div class="flash">
  The "default" Matrix homeserver is <code>matrix.org</code>, which is used by 35% of all Matrix users <a href="https://matrix.org/blog/2020/01/02/on-privacy-versus-freedom">as estimated in 2020</a>. Although it is okay to use it (and you can try out Matrix quickly), it is highly encouraged to choose a different homeserver (or run your own) for long-term usage, as it serves the spirit of decentralization promoted by the Matrix protocol, and also because <code>matrix.org</code> is occasionally overloaded (though performance has improved in recent times).
</div>
<br>
If you have hosting, and have the technical skills required to host an internet-facing program, then you can try setting up your own homeserver[^6]. The dominant homeserver implementation is [Synapse](https://github.com/matrix-org/synapse/). See [installation instructions](https://matrix.org/docs/guides/installing-synapse). It may be possible to run a homeserver for free [with Oracle Cloud](https://matrix.org/docs/guides/free-small-matrix-server).

However, hosting is still unreachable for many. In that case, you can join an existing homeserver by picking one from [our public homeserver list](../servers), or by contacting a friend who hosts one.

### Register an account

<div class="flash">
  This part does not cover cases where a homeserver uses their own authentication tools. In such cases, please consult related information of the homeserver in question.
</div>
<br>
For simplicity, the guide is prepared in such a way that recommends registration on a PC browser, even though many servers allow you to do so from native PC/mobile apps. Regardless, once registered, you can use the account everywhere!

1. If our homeserver list already provided you with a link to the homeserver's in-house Element client, then you may use that. Otherwise, use the official [Element Web client](https://app.element.io) to register.
2. Click "Create Account".
3. On the top of the registration dialog, verify that you are registering on the correct server. If necessary, click "edit" and enter the appropriate domain (see homeserver documentation or the "Registration method" column of the [homeserver list](../servers)). Once it is correctly entered, **note the domain down.** You will need it to login.
4. Fill out the required information.
5. If you did not enter an email address, then you're in. Otherwise, verify your email, after which you will be prompted to [login](#log-into-an-existing-account).

Remember to [set up key backup](#set-up-key-backup)!

### Log into an existing account

For most clients:

1. Enter the login dialog, if necessary.
2. Verify that you are logging onto the correct server. This is usually shown on top of the dialog. If necessary, click "edit" and enter the appropriate domain (see Step 3 of registration).
3. Enter your login details. The username is the part after the at-mark and before the colon (called "localpart").

### Set up key backup

When you log into a new device, you will be prompted to verify it using your existing device (by scanning a QR code or by comparing emojis). Your new device will then retrieve the room keys from your existing device, thereby enabling it to read your encrypted messages. This prevents anyone else - including your homeserver operator - to read encrypted content[^1].

A Security Key is required to access encrypted messages if:

* You have previously logged out of *all* your sessions, or
* You are unable to verify interactively from another session.
<br>
<div class="flash flash-warn">
It is <b>strongly recommended</b> to do this step to prevent accidentally losing all of your encrypted messages.
</div>
<br>
1. On your first login, a bubble on the top-left will ask you to "set up secure backup". Click "Continue". If that is not the case, click your avatar, then "Settings" -> "Security & Privacy" -> "Secure Backup" -> click "Set up".
2. "Generate a Security Key" is enough.
3. Put the generated security key in a safe place.

## Get Familiar

### What clients should I use?

Matrix.org has [a list of clients](https://matrix.org/clients/). However, it's... a bit messy. So here's a quick rundown on clients that we recommend:

#### Browser

* [Element](https://app.element.io): The flagship client.
  * [Element development version](https://develop.element.io): Element with lab features enabled.
  * [SchildiChat](https://app.schildi.chat/): Element with lab features enabled, plus an optional speech bubble layout.
* [Cinny](https://cinny.in/): Matrix in Slack style.
* [Hydrogen](https://hydrogen.element.io/): Fast and adaptable to mobile browsers, at the cost of missing some optional features.

#### PC

The author of this guide recommends either [Element](https://element.io) or [SchildiChat](https://schildi.chat/) for supporting the most features.

* [Element](https://element.io): The flagship client.
  * [SchildiChat](https://schildi.chat/): Element with lab features enabled, plus an optional speech bubble layout.
* [FluffyChat](https://fluffychat.im/): "Cute" Matrix.

For those living on the edge: [Nheko](https://github.com/Nheko-Reborn/nheko) and [Spectral](https://spectral.im)

#### Mobile

The author of this guide recommends [FluffyChat](https://fluffychat.im) for performance.

* [Element](https://element.io): The flagship client.
  * [SchildiChat](https://schildi.chat/): Element with lab features enabled, plus an optional speech bubble layout.
* [FluffyChat](https://fluffychat.im/): "Cute" Matrix.

For those living on the edge: [Syphon](https://syphon.org/)

### What rooms should I join?

Each Matrix homeserver has a public room directory, which is accessible to the users of that homeserver or, if enabled, users of other homeservers as well.

* On PC, for Element and SchildiChat, click the "Explore Rooms" button below your username on the top-left.
* On phone, for Element and SchildiChat, click the "Explore Rooms" floating button on the bottom-right.
* For FluffyChat, click the search button.

In any case mentioned above, you can enter the room address to directly join a room, or you can enter keywords to search for rooms[^7]. However, the directory may be unintuitive to use as it orders rooms by member count[^8]. The author of this guide recommends joining [this Space](https://matrix.to/#/#offtopic-space:envs.net) (`#offtopic-space:envs.net`), which contains a list of active off-topic or no-topic discussion rooms.

#### Hold on, what's a Space? Why is it on the left of my room list?

Discord users may be familiar with this format, but Spaces are not exactly the same as a Discord "server". A Space[^9] is a list that can include other rooms and Spaces. It can be used to organize your own rooms, or for a community to organize all their rooms. Joining a Space does not imply joining all of its rooms (however, rooms can choose to require users to join a Space first), nor does leaving a Space imply leaving all of its rooms (although you can configure your client to do so).

### Go Deeper

(introducing other pages...)

## Footnotes

[^1]: Only text contents and file attachments of messages are encrypted. Currently, Matrix does not prevent metadata leakage, mainly due to its federated nature. This will change, however, when Matrix starts rolling out [Pinecone](https://archive.fosdem.org/2021/schedule/event/matrix_pinecones/), allowing p2p connections. Currently, it *can* be mitigated if all participants of an E2EE conversation are running their own homeserver (so to eliminate third parties).

[^2]: Exception: Some bots do not support end-to-end encrypted messaging. Furthermore, when creating an empty private room, you will be prompted (but not by default) to enable encryption.

[^3]: Element allows you to opt into (not enabled by default as of late 2021) using an "identity server" - think of it as a big online address book. This allows users to share their email addresses and username, which can be looked up manually by other users. However, here "contacts" only mean the address book on smartphones; homeservers *can* see who you are talking to, as such information are not encrypted. There is [a proposal](https://github.com/matrix-org/matrix-doc/pull/3414) to address this. See also footnote 1.

[^4]: Note that public rooms may block certain servers - just like banning individual users - due to prevalence of unacceptable content (spam, hate speech, etc.). If you're not running your own homeserver, don't join homeservers that are known to harbour such content. This does not apply to homeservers listed on [our public list](../servers) as they are vetted against any presence of bad reputation. In any case, behave yourselves, remember the human.

[^5]: This covers all the ones that an average user sees.

[^6]: Synapse is the only stable homeserver implementation as of now. If you are living on the edge, you can try out [Dendrite](https://github.com/matrix-org/dendrite/) and [Conduit](https://conduit.rs/), both of which aim to support p2p eventually (see footnote 1).

[^7]: Title and description.

[^8]: Which is not a reasonable gauge of activity. First, accounts can be inactive. Second, if a server uses bridges, then these accounts are counted as well, even if their activity is mostly not from Matrix (you can still interact with them, however).

[^9]: Which, to be exact, is a special type of rooms. But that's too technical, so this guide will treat Space as its own thing, although similar to rooms.