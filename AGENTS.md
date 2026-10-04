# securityLab — 25 Landing Pages

## The idea
A landing page for securityLab, a cybersecurity company selling modular, pay-as-you-go security products. "securityLab" is a placeholder name; keep it easy to find-and-replace.
- **Who it's for:** any visitor to the site, human or AI agent: small business owners (especially tech), indie software developers, vibe coders, and AI agents acting for them. They want authentication security primitives on reasonable pay-as-you-go terms, without a large contract or a sales call.
- **What a visitor should understand or do:** try the products. Every product can be registered for and paid for instantly, as needed.

## The product
- Focus: supplementing existing authentication systems with threat data.
- Flagship: **whereami**, login-time detection. For each account login attempt it returns a real-time risk analysis of the observed IP address and other metadata, with high precision and recall.
- Pricing model: usage-based, no contract. Exact prices are placeholders; label them as such.

## Design direction
- The bar: every version should pass as a real, production landing page for a real company.
- Tone references: Palantir, Anduril (restraint, confidence). Structure references: developer-first companies like Stripe, Clerk, Resend (code in the hero, visible pricing, instant signup).
- Anti-references: Mandiant, CrowdStrike (enterprise-sales pages for a very different buyer).
- A theme is an accent, never a costume. No metaphors running through every button and label.
- A real page answers within seconds: what it is, who it's for, why trust it, what to do next. Show the product (API calls, responses, dashboards) rather than decoration.
- AI agents are first-class visitors: key facts (endpoints, pricing, signup) should be easy for an agent to find and parse.

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
