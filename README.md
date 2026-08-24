# dancersdna.com — the holding page

The public page at **dancersdna.com** until the product opens. Built from Claude
Design's handoff (`design_handoff_coming_soon/README.md`, 2026-08-24), as a
plain static page: no framework, no build step, nothing to go stale.

## Why it is not part of the main app

Pointing the domain at the app would publish the whole product under the real
brand name while it is still Stage 0 — every page, indexable. This is one page
that says one thing, hosted on its own, so the domain can be live long before
the product is.

## Two things it does differently from the design file, both deliberate

**Fonts are served from this repo, never from Google.** The design links
`fonts.googleapis.com`. dancersdna decided not to send a visitor's IP to a third
party before they have done or agreed to anything, and this page is the *first*
thing a stranger loads at the real domain.

**A question is not yet promised a reply.** The design's prototype opened the
visitor's own mail app addressed to `hello@dancersdna.com` — an address that
cannot receive anything, because the domain has sending records and **no MX
record at all**. The handoff says to replace it with a real submission; that
endpoint stores a stranger's email or Instagram handle, so it is with House
Counsel before it is built. Until then `SUBMIT_ENDPOINT` is `null` and the flow
says plainly that nothing was sent, rather than thanking someone for a message
that went nowhere.

## Deploying

GitHub Pages serves `main`. `CNAME` holds the custom domain. There is no build.
