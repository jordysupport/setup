# Site conventions and the URL contract

This file is the contract that keeps jordysupport.com free of broken links.
Read it before adding, renaming, or restructuring anything. It was written
2026-08-10 after a full link audit; the rules encode why that audit came
back clean.

## The URL contract

1. **Page URLs are permanent.** Once a page ships, its slug never changes.
   External surfaces (Ko-fi, YouTube descriptions, social posts, Linktree)
   and other sites link to pages, and 14+ internal pages cross-link them.
   If a rename is ever unavoidable, add the old URL to the `redirects`
   plugin map in `mkdocs.yml` in the same commit, and keep that redirect
   forever.
2. **Download URLs are more than permanent.** GitHub Pages cannot redirect
   a binary (meta-refresh only works for HTML pages), so a renamed or
   deleted ZIP is a permanent 404 for everyone who saved the link.
   Files under `docs/downloads/` are never renamed and never deleted.
3. **Updates happen in place.** A new version of a playbook overwrites the
   same ZIP at the same URL, so the canonical link always serves the
   latest. Versioned filenames (`-v2.zip`) are forbidden; they are how
   broken-link sprawl starts.
4. **External surfaces link pages, never ZIPs.** Pages can carry a
   redirect if the worst happens; binaries cannot. Anything posted off:site
   points at `https://jordysupport.com/playbooks/<slug>/`, not at a
   `.zip`.
5. **The old domain still works.** `jordysupport.github.io` 301s to
   `jordysupport.com` with paths preserved (verified 2026-08-10). New
   content always uses `jordysupport.com`.

## Playbook naming convention

Every playbook uses one slug everywhere. For slug `<slug>`:

| Surface | Value |
| --- | --- |
| Page | `docs/playbooks/<slug>.md` → `/playbooks/<slug>/` |
| Example page | `docs/playbooks/<slug>-example.md` |
| ZIP | `docs/downloads/<slug>-skill.zip` |
| Folder inside the ZIP | `<slug>-skill/` containing `INSTALL.md` + `SKILL.md` |
| Install target in the user's vault | `Skills/<slug>/SKILL.md` |
| Start phrase | set in `SKILL.md` frontmatter (`start-phrase`) |

## New playbook checklist

- [ ] Pick the slug; confirm it against the table above on every surface.
- [ ] ZIP contains exactly `<slug>-skill/INSTALL.md` and
      `<slug>-skill/SKILL.md`, plain text, **no URLs inside** (files with
      no URLs cannot rot).
- [ ] Page carries: `description` frontmatter, `software_schema` block
      (name, OS, category, `version`, `download_url`), the full text of
      `INSTALL.md` in the "What's inside this zip" disclosure, both install
      options, the checklists, and the version line under the download
      button.
- [ ] Example page built from the shared pattern; sample inputs are
      labeled as samples, real sources are real and checked.
- [ ] Add the page and its example to `nav` in `mkdocs.yml`.
- [ ] Add a row to the table in `docs/downloads/index.md`.
- [ ] `mkdocs build --strict` passes locally before pushing.

## Updating an existing playbook

- [ ] Overwrite the ZIP in place (same filename).
- [ ] Bump the version line on the page and `software_schema.version`,
      and note what changed in one sentence.
- [ ] Keep the "What's inside this zip" disclosure word-for-word identical
      to the shipped `INSTALL.md`.
- [ ] If Ko-fi Shop listings exist, re-upload the new ZIP to the matching
      listing (Ko-fi holds a copy; the site is canonical).

## Writing rules for public copy

- No em-dashes in drafted copy intended for publication or example
  outputs.
- Never claim an outcome, statistic, or testimonial that has not been
  measured or verified. Sample scenarios are labeled as samples.
- Free means free: no gated downloads, no required signup. The optional
  email list delivers new playbooks; it never locks them.
