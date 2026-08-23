# GlycoView

A mobile-first, installable web app prototype for visualizing oral glycopyrrolate timing.

## What it does
- Log dose amount, date/time, and food condition.
- Show a Theraview-style relative medication-activity timeline.
- Stack multiple doses mathematically.
- Show research-average clinical onset (~2.3 h) and duration (~7.4 h).
- Use fasting PK values (Tmax ~3.1 h, half-life ~3.0 h).
- Use a high-fat study condition (Tmax ~2.6 h, half-life ~3.2 h, peak ~26% of fasting).
- Persist entries locally on the device with localStorage.
- Does not recommend dosing or redosing.

## Run locally
Open `index.html` in a browser. For full install/offline PWA behavior, serve this folder from HTTPS (for example GitHub Pages, Netlify, or any static host).

## iPhone install
Once hosted on HTTPS:
1. Open the site in Safari.
2. Tap Share.
3. Tap **Add to Home Screen**.

## Model note
The activity graph is a visualization based on population pharmacokinetic averages, not a measured blood concentration or a validated predictor of sweat suppression. “Other / unknown food” intentionally does not use an invented food multiplier.

## Research basis
- FDA/DailyMed oral glycopyrrolate pharmacokinetic and food-effect data.
- Kim WO et al., *Effect of Oral Glycopyrrolate in Essential Hyperhidrosis* (mean onset 2.3 h; mean duration 7.4 h).

Use only according to your clinician's prescription.


## Version 2 UI
Adds a richer live activity hero, progress indicator, recent-dose chips, and clearer Theraview-style status language.


## Version 3 graph clarification
Bars after the research-average 7.4-hour clinical-effect window are faded and labeled as a pharmacokinetic tail rather than implied sweat-control activity. A marker shows where the mean clinical-effect window ends.


## Version 4 graph behavior
The displayed medication-activity bars stop completely after the published mean 7.4-hour clinical-effect duration for each logged dose. No pharmacokinetic tail is displayed.


## Version 5
Centered the activity-status badge and added meal-timing guidance (at least 1 hour before or 2 hours after meals) to the model explanation, with a formulation/prescription caveat.


## Version 6
Adds a full-day combined activity graph, up to four same-day dose status cards, % of today's predicted combined peak, and per-dose % of each dose's own modeled peak.


## Version 7
Supports 4–6 same-day logs visually with six chronological purple shades, from lightest for the earliest dose to darkest for the latest. The full-day graph stacks each dose's contribution in its matching shade.
