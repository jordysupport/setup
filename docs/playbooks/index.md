---
description: >-
  AI playbooks: teach your AI a job once — research, meeting notes, content — then run it any time with one phrase. Free downloads, plain English.
---

<div class="playbook-hero" markdown>

<span class="kicker">Playbooks</span>

# Teach your AI a job once. Use it forever.

A [playbook](../resources/glossary.md#playbook) is one useful job — research, meeting notes, content — packaged so your AI learns it in a minute and can run it any time you ask.

</div>

## How it works

<div class="playbook-steps">
  <div><strong>1 · Download</strong><span>Grab the small zip file for the playbook you want.</span></div>
  <div><strong>2 · Hand it over</strong><span>Open its page and copy the filename-specific install message. Your AI saves the playbook to your notes.</span></div>
  <div><strong>3 · Just ask</strong><span>From then on, say "start my research playbook." It interviews you — no forms, no re-downloads.</span></div>
</div>

That's the whole setup. The AI asks where you keep your notes, saves the playbook there, and tells you the start phrase to use forever.

!!! tip "No agent? No problem."
    Every playbook page also has a plain copy-paste prompt that works in any normal AI chat.

## The Library

Every playbook, free, installed the same way. Each one links a finished example, so you can see the payoff before you download anything.

<div class="library-list">
  <div class="library-row">
    <div class="library-info">
      <strong>Research a topic</strong>
      <span>One question in, a short brief with real sources out. 15–30 minutes.</span>
    </div>
    <p class="library-actions">
      <a class="md-button md-button--primary" href="research-brief/">Open</a>
      <a class="md-button" href="research-brief-example/">Example</a>
    </p>
  </div>
  <div class="library-row">
    <div class="library-info">
      <strong>Repurpose content</strong>
      <span>One article, video, or post becomes drafts for every channel. 10–20 minutes.</span>
    </div>
    <p class="library-actions">
      <a class="md-button md-button--primary" href="content-repurpose/">Open</a>
      <a class="md-button" href="content-repurpose-example/">Example</a>
    </p>
  </div>
  <div class="library-row">
    <div class="library-info">
      <strong>Process a meeting</strong>
      <span>Messy notes become decisions, to-dos, and a sendable follow-up. 10–15 minutes.</span>
    </div>
    <p class="library-actions">
      <a class="md-button md-button--primary" href="meeting-follow-up/">Open</a>
      <a class="md-button" href="meeting-follow-up-example/">Example</a>
    </p>
  </div>
  <div class="library-row">
    <div class="library-info">
      <strong>Build a knowledge base</strong>
      <span>Things worth keeping become short, sourced notes in your vault. 10–20 minutes.</span>
    </div>
    <p class="library-actions">
      <a class="md-button md-button--primary" href="knowledge-base/">Open</a>
      <a class="md-button" href="knowledge-base-example/">Example</a>
    </p>
  </div>
</div>

<div class="signup-panel">
  <span class="kicker">New playbooks, sent to you</span>
  <p>The library grows, and every playbook lands here free, no signup. Leave an email and new ones hit your inbox the day they ship, along with occasional practical tips and tools worth knowing about. Nothing sold, nothing shared, unsubscribe any time.</p>
  <form class="signup-form" action="https://app.kit.com/forms/9786057/subscriptions" method="post">
    <input class="signup-input" type="email" name="email_address" placeholder="Email address" aria-label="Email address" autocomplete="email" required>
    <button class="signup-button" type="submit">Subscribe</button>
  </form>
  <p class="signup-status" role="status" aria-live="polite" hidden></p>
</div>

<script>
(function () {
  var form = document.querySelector(".signup-form");
  if (!form) return;
  form.addEventListener("submit", function (e) {
    e.preventDefault();
    var status = document.querySelector(".signup-status");
    var button = form.querySelector(".signup-button");
    var fail = "That didn't go through. Check the address and try again.";
    button.disabled = true;
    fetch(form.action, {
      method: "POST",
      body: new FormData(form),
      headers: { Accept: "application/json" }
    }).then(function (r) { return r.json(); }).then(function (d) {
      if (d && d.status !== "failed") {
        form.querySelector(".signup-input").value = "";
        status.textContent = "Done. Check your email to confirm your subscription.";
      } else {
        status.textContent = fail;
      }
    }).catch(function () {
      status.textContent = fail;
    }).finally(function () {
      status.hidden = false;
      button.disabled = false;
    });
  });
})();
</script>

## Two rules that never change

1. **You review before anything is used, sent, or published.**
2. **The AI stays inside the folder you gave it.**

Every playbook ships with both baked in. And none of them hand you a form to fill out: each one interviews you one question at a time, in plain English, so you can't do it wrong.
