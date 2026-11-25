---
layout: about
title: About
excludeAutoH1: true

author: Ky
date: 2026-11-24 22:12

redirect-from:
    - about
    - contact
    - Contact
    - faq
    - FAQ

page-specific-stylesheets:
    - /styles/about.css
---


{%- for author in site.authors -%}
    {%- case author.role -%}
        {%- when "Creator", "Primary" -%}
            {%- assign primary = author -%}
    {%- endcase -%}
{%- endfor -%}



<!-- > Brands ain't friends. -->


> {{ site.brand.name | default: "This" }} is a brand (not a company).<br/>
> {{ primary.name | default: "The anonymous creator" }} uses this brand for {{ primary.pronouns.possessive-determiner | default: "their" }} bullshit-free apps which do the basics and do them well.
{:.hero}



## What is bullshit?

Can't say something's "bullshit-free" without defining bullshit, so here's **what you'll never find in {{ site.brand.name }} apps:**

<!-- I'd do a definition list (<dl>, <dt>, and <dd>) but I want to keep this page simple -->
- **Paywalls** 
  We might ask for donations and shit like that, but {{ site.brand.name | default: "our" }} apps will never stop you from using any feature of any app just because you're too poor to afford it.
- **Gambling** 
  "Ah yes let's exploit the most vulnerable people for profit. That's a great way to build trust!" I said lying. Fuck blind bags, fuck loot boxes, fuck prediction "markets", fuck crypto, fuck aaaalllllll that shit.
- **Jumpy UI** 
  You know when you go to tap something, and the UI suddenly shifts and you end up tapping something else? Yeah fuck that, {{ site.brand.name | default: "our" }} apps are designed from the ground up to avoid that as much as possible. That includes popup dialogs.
- **Required internet** 
  Oh my fucking gosh it is an _app_ installed _on my device_ it needs to be able to _do the thing_ even when I'm out in the middle of bumfuck nowhere with no Internet connection!
- **Random pointless AI no one asked for** 
  <span class="big">✨🫩</span>
- **Bloat** 
  Why the fuck does everything have an Instagram Stories ripoff? Why is Telegram littered with crypto shit? Fucking _LinkedIn has games!_ {{ site.brand.name | default: "Our" }} apps won't include any features they don't need.
- **Ads** 
  Not to say {{ site.brand.name | default: "we" }} won't _ever_ take sponsor money, but when we do, you won't see it and think "that's an ad". If I had a nickel for every time I saw that fucking king get crushed, I could afford whatever stupid premium upsell bullshit I'd need to pay to never see him get crushed again. But I probably still wouldn't pay that because it's _damn funny_ to watch a king get crushed for free and I can use that money pay for something actually good, like an artist's Patreon.
{:.bullshits}



## Contact info

{%- if site.social.default-username %}
As with everything, our social media handles are **{{ site.social.default-username }}**.
{%- endif %}



<section class="contact-cards   flex-row flex-wrap flex-horiz-center">
{%- if site.social.bsky %}

{%- assign bskyHref = "https://bsky.app/profile/" | append: site.social.bsky %}

{% include social/user-card.html
    service-name="Bluesky"
    username=site.social.bsky
    href=bskyHref
%}
{%- endif %}



{%- if site.social.telegram %}

{%- assign tgHref = "https://t.me/" | append: site.social.telegram %}

{% include social/user-card.html
    service-name="Telegram"
    username=site.social.telegram
    href=tgHref
%}
{%- endif %}



{%- if site.social.mastodon %}

{%- assign mastodonHref = "https://" | append: site.social.mastodon.instance | append: "/@" | append: site.social.mastodon.username %}
{%- assign mastodonUsername = site.social.mastodon.username | append: "@" | append: site.social.mastodon.instance %}

{% include social/user-card.html
    service-name="Mastodon"
    username=mastodonUsername
    href=mastodonHref
%}
{%- endif %}



{%- if site.social.github %}

{%- assign ghHref = "https://github.com/" | append: site.social.github %}

{% include social/user-card.html
    service-name="GitHub"
    username=site.social.github
    href=ghHref
    omit-at-sign-in-username=true
%}
{%- endif %}



{%- if site.social.email %}

{%- assign eHref = "mailto:" | append: site.social.email %}

{% include social/user-card.html
    service-name="eMail"
    username=site.social.email
    href=eHref
    omit-at-sign-in-username=true
%}
{%- endif %}
</section>
