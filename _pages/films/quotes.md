---
layout: page
title: Two Quotes
permalink: /films/quotes/
description: Favorite quotes from film industry professionals.
---

<style>
  .quote-section {
    position: relative;
    padding: 4rem 3rem;
    margin: 2rem 0;
    border-radius: 4px;
    overflow: hidden;
  }
  .quote-section::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.08'/%3E%3C/svg%3E");
    background-size: 200px 200px;
    pointer-events: none;
    z-index: 0;
  }
  .quote-section.dark {
    background-color: #0e0e0e;
    color: #e8e0d0;
    border-left: 4px solid #c8a96e;
  }
  .quote-section.light {
    background-color: #1a1a2e;
    color: #d4cfc8;
    border-left: 4px solid #7b9ec7;
  }
  .quote-mark {
    font-size: 8rem;
    line-height: 0;
    vertical-align: -2.5rem;
    opacity: 0.15;
    font-family: Georgia, serif;
    position: relative;
    z-index: 1;
  }
  .quote-text {
    font-family: 'Georgia', 'Times New Roman', serif;
    font-size: 1.35rem;
    line-height: 1.85;
    font-style: italic;
    letter-spacing: 0.01em;
    position: relative;
    z-index: 1;
    margin: 0.5rem 0 1.5rem;
  }
  .quote-attribution {
    font-family: 'Courier New', monospace;
    font-size: 0.85rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    opacity: 0.7;
    position: relative;
    z-index: 1;
  }
  .quote-attribution::before {
    content: "— ";
  }
  .quote-rule {
    border: none;
    border-top: 1px solid rgba(255,255,255,0.08);
    margin: 0;
  }
</style>

<div class="quote-section dark">
  <span class="quote-mark">&ldquo;</span>
  <p class="quote-text">I think I'm attracted to subjects that I'm afraid of. It's a way to approach things I am afraid of, things that bring fear in my heart, and try to understand them, try to deal with them. It's like demons. I try to approach it and understand it… I'm just visiting fears.</p>
  <p class="quote-attribution">Dennis Villeneuve</p>
</div>

<hr class="quote-rule">

<div class="quote-section light">
  <span class="quote-mark">&ldquo;</span>
  <p class="quote-text">I really subscribe to that old adage that you should never let the audience get ahead of you for a second. So if the film's abrasive and wrongfoots people then, y'know, that's great. But I hope it involves an audience. If not, that's my f*ck-up.</p>
  <p class="quote-attribution">P.T. Anderson</p>
</div>
