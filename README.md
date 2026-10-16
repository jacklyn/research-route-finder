# What kind of research should I do?

A six-question guide that helps product designers and PMs find the lightest responsible way to answer a research question. Answers lead to one of four routes:

1. **Use what we already know.** Existing research and data may already answer it.
2. **DIY study.** A focused, low-risk question you can run yourself.
3. **DIY with a UXR gut check.** Run it yourself after 15–20 minutes with Research.
4. **Partner with UXR.** Big or high-stakes decisions that need more rigor.

Everything runs in the browser. There's no backend, login, database or build step.

## Run it locally

Open `index.html` in a browser. That's it.

## Publish with GitHub Pages

1. In this repo, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to "Deploy from a branch".
3. Pick the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://<your-username>.github.io/research-route-finder/`.

Every change you commit to `main` republishes automatically.

Note: on a free GitHub account, Pages sites are public to anyone with the link.

## Where to edit things

All copy and logic live in `index.html`, inside the `<script>` near the bottom. Each block is labeled with a numbered comment.

| What you want to change | Look for |
| --- | --- |
| Questions and answer options | `1. CONTENT: QUESTIONS` → `QUESTIONS` |
| Research methods (usability, concept, etc.) | `2. CONTENT: METHODS` → `METHODS` |
| Maze guidance, "How to run it" | `2b.` → `HOW_TO_RUN`, `STUDY_MODES`, `INTERPRETATION` |
| Sample questions to try and avoid | `2c.` → `SAMPLE_QUESTIONS`, `QUESTION_TIPS` |
| Result headlines, next steps, "Bring Research" lists | `3. CONTENT: ROUTES` → `ROUTES` |
| Intro question prompt, copy-summary messages | `INTRO_PROMPT`, `COPY_TEXT` |
| Which answers lead to which route | `4. RULES` → `RULES` |
| "See how we got here" explanations | `5.` → `FACTORS` |

### How the rules work

Routes are checked in this order, and the first match wins:

1. `existing`: all of its conditions must be true.
2. `partner`: any one condition is enough.
3. `gutCheck`: any one condition is enough.
4. `diy`: the default when nothing above matched.

Each condition has a `test` (which answers trigger it) and a `reason` (the text shown under "Why you got this result"). To add a rule, copy an existing condition and change both. If someone answers "Maybe?" to the evidence question, they see a quick check before their result.

### Styling

Colors and fonts are defined as tokens at the top of the `<style>` block (`:root`), with dark-mode values right below. Change the accent by editing `--accent` in both places.

## Tech

React 18 and [htm](https://github.com/developit/htm) load from public CDNs, so the app needs no build tools. Fonts come from Google Fonts.
