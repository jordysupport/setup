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

After you download, open that playbook's page and copy its install message. The exact downloaded filename is already filled in, so your AI knows what to locate and extract.

That's the whole setup. The AI will ask where you keep your notes, save the playbook there, and tell you the magic phrase to start it later.

!!! tip "No agent? No problem."
    Every playbook page also has a plain copy-paste prompt that works in any normal AI chat.

## Pick a playbook

<div class="grid cards" markdown>

-   **Research a topic**

    You answer a few questions. It comes back with a short brief and real sources.

    [Open playbook →](research-brief.md){ .md-button .md-button--primary }

-   **Repurpose content**

    One source in, drafts for newsletter, social, and video out.

    [Open playbook →](content-repurpose.md){ .md-button .md-button--primary }

-   **Process a meeting**

    Notes in, decisions, to-dos, and a draft follow-up out.

    [Open playbook →](meeting-follow-up.md){ .md-button .md-button--primary }

-   **Build a knowledge base**

    Turn something worth keeping into a clean note in your vault.

    [Open playbook →](knowledge-base.md){ .md-button .md-button--primary }

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

## Why the interview beats a form

Old way: copy a prompt, fill in `[the blanks]`, hope you guessed the format right. New way: the AI asks you one question at a time, in plain English, and fills in the playbook itself. You can't do it wrong.

## Two rules that never change

1. **You review before anything is used, sent, or published.**
2. **The AI stays inside the folder you gave it.** Every playbook is built with those rules baked in.
