# ericbackman.github.io

Source for **[ericbackman.github.io](https://ericbackman.github.io/).** My
personal site: background, experience, skills, and a hub linking the projects I
actually run.

> **Not the primary domain.** [ericbackman.com](https://ericbackman.com) is
> served by [ai-resume](https://github.com/ericbackman/ai-resume), an MCP server
> that answers questions about my work conversationally. This repo is the static
> GitHub Pages version.

## How it's built

Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies to
install: edit a file, push, and GitHub Pages redeploys.

```
index.html        the whole page (sections + the Live projects hub)
css/style.css     dark theme, JetBrains Mono
js/main.js        nav toggle, scroll behaviour, hub rendering
projects/         project detail page
assets/           favicon
```

## Deployment

GitHub Pages builds from **`master`**, repo root. Push to `master` and it's live
within a minute or two: there is no staging step, so preview locally first:

```bash
python -m http.server 8000
```

Note the branch is `master`, not `main`: a Pages setting, easy to trip over when
a change looks pushed but never appears.

## The Live hub

The "Live" section renders from an array in `index.html`, one entry per site I
host on `*.ericbackman.com`, grouped by category. Adding a site is one object:

```js
{ cat: "Games", name: "2048.ericbackman.com",
  url: "https://2048.ericbackman.com",
  desc: "Merge Tiles — 2048 with a swappable merge-rule engine" }
```

**Before adding an entry, check what listing it actually discloses.** This page is
public and search-indexable, so a link here publicly associates that site, and
whatever it's for, with my name. Several sites I run are deliberately gated,
pseudonymous, or personal, and belong in the private
[link-hub](https://links.ericbackman.com) instead. The gate on a site protects its
*contents*; it does not hide that the site exists or what it's for.

## Related

| Repo | Serves |
|---|---|
| [ai-resume](https://github.com/ericbackman/ai-resume) | ericbackman.com + www + ai. (the primary site) |
| link-hub | links.ericbackman.com: private index of everything hosted |
| [dive-map](https://github.com/ericbackman/dive-map) | the dive map linked from here |
