# securityLab — 25 Landing Pages

## The idea
A landing page for securityLab, a cybersecurity lab/company. "securityLab" is a placeholder name; keep it easy to find-and-replace.
- **Who it's for:** TODO
- **What a visitor should understand or do:** TODO

## Goal
Build 25 distinct versions of this landing page (`v01`–`v25`), plus a gallery (`index.html`) that tells the story of the process.
- **v01–~v12, go wide:** radically different directions in layout, audience, mood, era and tone. A change of colors or fonts alone is not a new direction.
- **Middle versions, narrow down:** iterate on what works for the visitor and combine strengths (e.g. v05's type with v11's layout).
- **v20–v25, converge:** refine until v25 is the final choice.
- Every version should be distinctive. Avoid generic AI-landing-page looks.

## Constraints
- Plain HTML and CSS, optional vanilla JS. **No frameworks, packages, build step, external APIs, or data storage.** Push back if tempted.
- Any content (stats, case studies, findings) is written by hand into the page (no fetching). Keep it plausible and label invented data as illustrative.

## Structure
```
index.html          gallery: grid of v01–v25, each with a thumbnail, a link, and a one-line note on what changed;
                    tells the process story and presents the final choice
v01/index.html      each version is self-contained (own CSS/JS inline or in its folder)
...
v25/index.html
```
Every version page has a visible "← Gallery" link back to `/` and shows its version number.

## Pipeline
Edit locally → `git commit` → `git push` (SSH remote) → Vercel auto-deploys.
- Repo: https://github.com/kenpiech/securityLab
- Live: https://securitylab-kenpiech.vercel.app
