---
layout: page
title: Discussion Forum
permalink: /films/discussion-forum/
description: Discussion board for classmates.
---

<style>
  .forum-page {
    background-color: #0a0a0a;
    color: #ddd6c8;
    padding: 3rem 2.5rem;
    border-radius: 4px;
    position: relative;
    overflow: hidden;
    font-family: 'Georgia', 'Times New Roman', serif;
  }
  .forum-page::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.06'/%3E%3C/svg%3E");
    background-size: 200px 200px;
    pointer-events: none;
    z-index: 0;
  }
  .forum-page > * { position: relative; z-index: 1; }

  .forum-page h2 {
    font-family: 'Courier New', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #c8a96e;
    margin-bottom: 0.25rem;
  }
  .forum-page h1 {
    font-family: Georgia, serif;
    font-size: 2.2rem;
    font-weight: normal;
    color: #f0ebe0;
    margin-top: 0;
    margin-bottom: 0.75rem;
    border-bottom: 1px solid rgba(200,169,110,0.3);
    padding-bottom: 1rem;
  }
  .forum-intro {
    font-size: 1.05rem;
    line-height: 1.8;
    color: #b8b0a0;
    margin-bottom: 2rem;
  }
  .form-wrapper {
    border-radius: 4px;
    overflow: hidden;
    border: 1px solid rgba(200,169,110,0.2);
    box-shadow: 0 4px 30px rgba(0,0,0,0.5);
    margin-bottom: 3rem;
  }
  .form-wrapper iframe {
    display: block;
    width: 100%;
    border: none;
  }

  /* Comments section */
  .comments-heading {
    font-family: 'Courier New', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #c8a96e;
    margin-bottom: 1.25rem;
    border-top: 1px solid rgba(200,169,110,0.2);
    padding-top: 2rem;
  }
  .comment-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(200,169,110,0.12);
    border-left: 3px solid #c8a96e;
    border-radius: 3px;
    padding: 1.25rem 1.5rem;
    margin-bottom: 0.5rem;
  }
  .comment-name {
    font-family: 'Courier New', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #c8a96e;
    margin-bottom: 0.4rem;
  }
  .comment-text {
    font-size: 1rem;
    line-height: 1.7;
    color: #d4cfc8;
  }
  .response-card {
    background: rgba(123,158,199,0.05);
    border: 1px solid rgba(123,158,199,0.15);
    border-left: 3px solid #7b9ec7;
    border-radius: 3px;
    padding: 1rem 1.5rem;
    margin-bottom: 1.5rem;
    margin-left: 1.5rem;
  }
  .response-name {
    font-family: 'Courier New', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #7b9ec7;
    margin-bottom: 0.35rem;
  }
  .response-text {
    font-size: 0.97rem;
    line-height: 1.7;
    color: #c0bdb8;
  }
  .comments-loading {
    color: #7a7060;
    font-style: italic;
    font-size: 0.95rem;
  }
  .comments-error {
    color: #8a6a4a;
    font-style: italic;
    font-size: 0.9rem;
  }
  .refresh-btn {
    background: transparent;
    border: 1px solid rgba(200,169,110,0.4);
    color: #c8a96e;
    font-family: 'Courier New', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 0.4rem 1rem;
    cursor: pointer;
    border-radius: 2px;
    margin-bottom: 1.5rem;
    transition: background 0.2s;
  }
  .refresh-btn:hover { background: rgba(200,169,110,0.1); }
</style>

<div class="forum-page">
  <h2>Discussion</h2>
  <h1>Leave a Comment</h1>
  <p class="forum-intro">Share your thoughts on my films, ask questions, or leave feedback. No account required — just your name and a comment.</p>

  <div class="form-wrapper">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLScGMRyI8HqzAuRwLt9s36oAbceVRyKQsUh4uI9WMU3FKqLO0g/viewform?embedded=true"
      height="520"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      loading="lazy">
      Loading…
    </iframe>
  </div>

  <!-- Published comments -->
  <p class="comments-heading">Comments</p>
  <button class="refresh-btn" onclick="loadComments()">↻ Refresh comments</button>
  <div id="comments-container">
    <p class="comments-loading">Loading comments…</p>
  </div>
</div>

<script>
  const SHEET_ID = "1BrZbSRnNAFLcbo5Oxmpbd8Pr6uuvmOSuquxXkpB6Hdg";

  function loadComments() {
    const container = document.getElementById("comments-container");
    container.innerHTML = '<p class="comments-loading">Loading comments…</p>';

    const callbackName = "_gsCallback_" + Date.now();

    // Build the URL with ONE tqx param using responseHandler for JSONP
    const url = `https://docs.google.com/spreadsheets/d/${SHEET_ID}/gviz/tq?sheet=Form_Responses&tqx=out:json;responseHandler:${callbackName}`;

    window[callbackName] = function(data) {
      delete window[callbackName];
      const s = document.getElementById("gviz-script");
      if (s) s.remove();
      try {
        const rows = data.table.rows;
        if (!rows || rows.length === 0) {
          container.innerHTML = '<p class="comments-loading">No comments yet — be the first!</p>';
          return;
        }
        // col 0=Timestamp, col 1=Name, col 2=Comment, col 3=Response; newest first
        const cards = [...rows].reverse().map(row => {
          const name     = row.c[1] && row.c[1].v ? String(row.c[1].v) : "Anonymous";
          const comment  = row.c[2] && row.c[2].v ? String(row.c[2].v) : "";
          const response = row.c[3] && row.c[3].v ? String(row.c[3].v) : "";
          if (!comment) return "";
          const replyHTML = response
            ? `<div class="response-card">
                <div class="response-name">↳ William Hayward</div>
                <div class="response-text">${escapeHTML(response)}</div>
               </div>`
            : "";
          return `<div class="comment-card">
            <div class="comment-name">${escapeHTML(name)}</div>
            <div class="comment-text">${escapeHTML(comment)}</div>
          </div>${replyHTML}`;
        }).filter(Boolean).join("");
        container.innerHTML = cards || '<p class="comments-loading">No comments yet — be the first!</p>';
      } catch(e) {
        container.innerHTML = `<p class="comments-error">Parse error: ${e.message}</p>`;
      }
    };

    const script = document.createElement("script");
    script.id = "gviz-script";
    script.src = url;
    script.onerror = () => {
      container.innerHTML = "<p class=\"comments-error\">Could not load comments. Make sure the sheet is shared as 'Anyone with the link can view.'</p>";
    };
    document.body.appendChild(script);
  }

  function escapeHTML(str) {
    return String(str).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;").replace(/"/g,"&quot;");
  }

  loadComments();
</script>

