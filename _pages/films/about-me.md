---
layout: page
title: About Me
permalink: /films/about-me/
description: About me as a filmmaker.
---

<style>
  .film-page {
    background-color: #0a0a0a;
    color: #ddd6c8;
    padding: 3rem 2.5rem;
    border-radius: 4px;
    position: relative;
    overflow: hidden;
    font-family: 'Georgia', 'Times New Roman', serif;
    font-size: 1.08rem;
    line-height: 1.9;
  }
  .film-page::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.06'/%3E%3C/svg%3E");
    background-size: 200px 200px;
    pointer-events: none;
    z-index: 0;
  }
  .film-page > * { position: relative; z-index: 1; }

  .film-profile-img {
    float: left;
    width: 220px;
    margin: 0 2rem 1.5rem 0;
    border-radius: 3px;
    border: 2px solid #c8a96e;
    box-shadow: 0 0 30px rgba(200, 169, 110, 0.2), 0 4px 20px rgba(0,0,0,0.6);
  }
  .film-page h2 {
    font-family: 'Courier New', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #c8a96e;
    margin-bottom: 0.25rem;
    font-style: normal;
  }
  .film-page h1 {
    font-family: Georgia, serif;
    font-size: 2.2rem;
    font-weight: normal;
    color: #f0ebe0;
    margin-top: 0;
    margin-bottom: 1.75rem;
    border-bottom: 1px solid rgba(200,169,110,0.3);
    padding-bottom: 1rem;
  }
  .film-page p { margin-bottom: 1.4rem; }
  .film-page em { color: #c8a96e; font-style: italic; }
  .film-section-divider {
    border: none;
    border-top: 1px solid rgba(255,255,255,0.07);
    margin: 2rem 0;
  }
  .clearfix::after { content: ""; display: table; clear: both; }
</style>

<div class="film-page">
  <h2>Filmmaker</h2>
  <h1>William Hayward</h1>

  <div class="clearfix">
    <img src="{{ 'assets/img/profilepic.png' | relative_url }}" alt="William Hayward" class="film-profile-img">

    <p>My name is William Hayward, and I am a student filmmaker. As a beginner to filmmaking, I wear many hats each of my projects as I explore my creative strengths and interests. I have experience screenwriting, producing, and editing films, but my expertise lies in the latter of those three. I am primarily interested in developing my editing skills, particularly in the realm of sound(track) design. I am a team player, and work closely with my directors and screenwriters to ensure their creative vision is maximized to the fullest. No matter which role I take on, I always keep the end product in mind. For example, if I am editing, I provide input to the cinematographer about what shots could look good in post-production, but as the storyboarder, I always give flexibility to the other creatives in how they want to approach a scene.</p>
  </div>

  <hr class="film-section-divider">

  <p>My biggest influences and idols in filmmaking are Trent Reznor, Dennis Villeneuve, and P.T. Anderson. I appreciate their contributions to the filmmaking world because of their distinctly atmospheric style within their respective creative disciplines. Villeneuve, for example, has an excellent cinematographic eye that slows down an otherwise fast-paced movie. In a similar vein, P.T. Anderson is equally talented in worldbuilding, though I appreciate how his impeccable character writing contributes to the overall atmosphere of his works. Lastly, I am a huge fan of Trent Reznor, and by association, Atticus Ross. They are experts of creating driving electronic music that perfectly fits with a dramatic film, and I have even used their work in my own films.</p>

  <p>These three influences shape how I approach a film. Often times when shooting, I have a scene from one of their movies in my mind that I try to emulate stylistically. Anderson's character writing naturally creates a good arc, Villeneuve's eye creates aesthetically pleasing scenes, and Reznor's music compliments the emotion of the visuals. Keeping the vision of these key figures in mind, I am proud of the work I have done as a writer and editor. They all show in my films: <em>The Hunt</em>, <em>Gimghoul or Nothing</em>, and <em>Dirty Dishes</em>.</p>

  <hr class="film-section-divider">

  <p>I am proud of the work I did in all of those films. In <em>The Hunt</em>, I was a blogger for the film. I set up this website solely for the film, and put in a lot of work familiarizing myself with Bootstrap and GitHub websites. I am a statistics major, so I was very familiar with coding, but HTML and CSS are completely different, and it requires creativity. In <em>Gimghoul or Nothing</em>, I was the editor. I learned how to use DaVinci Resolve and spent a lot of time mastering audio levels and making decisions about what we shot would work best in each scene, and it really pulled together the movie. <em>Dirty Dishes</em> was a lot of fun for me because I wrote the entire script and starred in it. This was the first time I acted in a movie, and I worked extensively with my team to ensure my performance worked.</p>

</div>