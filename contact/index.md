---
layout: page
main-title: Contact The Experiment
sub-title: What, why, where and how?
description: "TBC"
keywords: "Lorenzo Sapora, contact, gpg, pgp, public key, email, twitter, skype, gitlab, git, sudosushi"
---

Found a bug? Have an interesting project? Or just want to chat, let's do it!

#### Best way to contact me

<p>{% include assets/contact/twitter.svg %} <a href="https://twitter.com/{{ site.twitter_username }}" title="Twitter">@{{ site.twitter_username }}</a></p>

<p>{% include assets/contact/skype.svg %} <a href="skype:{{ site.skype_username }}?chat" title="Skype">{{ site.skype_username }}</a></p>

<p>{% include assets/contact/gitlab.svg %} <a href="{{ site.url }}/git/" title="Gitlab">Git versioning</a></p>

<p>{% include assets/contact/gpg.svg %} <a href="{{ site.url }}{{ site.gpg_publickey }}" title="PGP Public key">Public key</a> for <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>

<p>{% include assets/contact/fingerprint.svg %} <code>{{ site.gpg_fingerprint }}</code></p>
