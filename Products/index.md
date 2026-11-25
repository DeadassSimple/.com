---
layout: page
title: Products
excludeAutoH1: true

author: Ky
date: 2026-11-25 01:00

redirect-from:
    - apps
    - Apps

page-specific-stylesheets:
    - /styles/products.css
---


{::nomarkdown}
{% include product-section-start.html
    id="main"
    title="Products™ by Brand™"
%}

{% include product-list-item-large.html
    url="https://GitHub.com/DeadassSimple/MediaPlayer"
    image-url="/images/MediaPlayer-thumbnail.webp"
    image-full-bleed=true
    title="Media Player"
    description="Just a basic local media player"
%}

{%- include product-list-item-large.html
    url="https://GitHub.com/DeadassSimple/"
    _x_image-url="/images/MediaPlayer-thumbnail.webp"
    image-full-bleed=true
    title="And more in the future"
    description="Probably. Hopefully."
%}

{%- include product-section-end.html %}
{:/nomarkdown}
