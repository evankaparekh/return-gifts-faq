# Return Gifts · Period Questions

A mobile-friendly, English/Spanish menstrual-health FAQ. Static HTML, CSS, and JavaScript; no API keys, build step, or subscription.

**Status: review draft.** Medical content, emergency wording, and Spanish translations require professional review before promotion as a public health resource. Linked organizations have not endorsed this project.

## Features

- 49 source-linked questions, searchable by words in questions and answers
- Five topic filters, English/Spanish interface, expandable answers
- Always-visible care guidance; no symptom assessment or diagnosis
- No generated medical answers; unmatched searches produce an explicit empty state
- No account, analytics, cookies, local storage, or question submissions
- Responsive layout, semantic controls, keyboard focus, screen-reader result count

## Run

Open `index.html` directly in a browser, or run `python3 -m http.server 8000` in this folder and visit http://localhost:8000. Search works offline; external sources need internet access.

## Publish with GitHub Pages

In repository **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, then **Save**. GitHub will show the final URL after deployment. Expected address: https://evankaparekh.github.io/return-gifts-faq/ . This repository does not enable Pages automatically.

Publishing makes this review draft accessible publicly. Complete the review checklist before presenting it as reviewed educational content. Do not remove the draft labels until both reviews are complete.

## Edit content

`faq-data.js` defines the sources, English/Spanish answers, topic, optional search keywords, and review metadata. It loads as a local script so opening the HTML directly works. `app.js` contains UI translations and care guidance. `styles.css` controls appearance.

Search matches all entered words within the chosen language and topic, ignoring accents and capitalization. It is keyword search, not an AI chatbot or triage tool. A failed search does not mean symptoms are safe. Care guidance stays visible for every search.

## Sources and review

See `CONTENT_REVIEW.md` for the source inventory, access limitations, and approval process. Source-check dates: October 1, 2026 (original questions), and October 4, 2026 (30 new questions). This date is not a clinician review date. Spanish is a draft translation, not an official translation of the cited organizations.

## Privacy

The application sends no search text over the network. No external fonts, scripts, embedded media, or trackers are loaded. Hosting providers can log visits (including IP addresses); source links navigate to third-party privacy policies. Do not enter names or other identifying information. Browser extensions and device history are outside this application's control.

## Verification

Run `node --check app.js` and `node --check faq-data.js`. DOM-level checks passed for search, accent normalization, topic filters, empty-state reset, language switching, arbitrary search text, and persistent care guidance. JavaScript syntax checks passed. Full browser rendering, keyboard, and mobile overflow checks remain to be performed; a browser executable was unavailable in the build environment.

## Scope

General menstrual education, not diagnosis, treatment selection, emergency monitoring, or a confidential medical service. Local resource availability and costs vary. The care directory is U.S.-focused; emergency wording identifies the U.S. number separately.
