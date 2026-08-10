---
hide_support_outro: true
description: >-
  Prompt Academy: the free newsletter from Jordy Support. One practical AI habit per issue, new playbooks the day they ship, plain English, every two weeks.
---

<span class="kicker">Newsletter · Every two weeks · Free</span>

# Prompt Academy

One practical thing worth doing with AI, what shipped on this site, and the occasional tool worth an honest take. Plain English, under a two-minute read, every two weeks.

<div class="signup-panel">
  <span class="kicker">Get Prompt Academy by email</span>
  <p>Every issue lands here free either way. Subscribers get it in their inbox, and new playbooks arrive the day they ship. Nothing sold, nothing shared, unsubscribe any time.</p>
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

## Every issue

- **One thing worth doing**: a practical habit or workflow, not news.
- **What shipped**: new playbooks and guides, the day they go up.
- **Worth knowing**: tools with honest takes, only things actually used here.
- **A question answered**: reply to any issue and yours can be next.

## The archive

Every issue lives here free, subscriber or not.

- [Issue #001: Ask it twice](001.md) · August 2026
