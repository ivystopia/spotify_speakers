# Codex brief for the Spotify speaker research project

This file is for you, not for Codex.

The goal is to give Codex one strong project brief that is complete enough to work from scratch, but not so rigid that it wastes effort following a brittle script. OpenAI's current description of Codex is that it can start from a prompt or spec, navigate a repo, edit files, run commands, and execute tests. GPT-5.4 in Codex is positioned for long-horizon, tool-using work across software environments, and Codex can also be given internet access in supported environments. That is why the main prompt below is outcome-oriented rather than micro-managed.

## Recommended setup before you send Prompt 1

- Model: GPT-5.4
- Reasoning: xHigh, or the highest available setting in your Codex surface
- Internet access: enabled if your surface supports it
- Workspace: a fresh directory for this project
- Permissions: enough for Codex to create files, install tools if needed, and browse the web
- Version control: ideal but not mandatory

## Suggested workspace goal

You want Codex to behave like a careful research operator with its own scratchpad. A good result is not just one chat reply. A good result is:

- a final human-readable report
- a structured candidate list
- a structured Spotify-verification log
- saved notes on unresolved questions or conflicts

You do not need to force an exact file layout, but if Codex wants a structure, a sensible one is:

- `notes/`
- `data/`
- `report/`
- `artifacts/`

## Important strategic note

Do not over-steer it with a brittle multi-mode workflow. This is one of the main reasons to use Codex instead of ChatGPT deep research plus manual handoffs.

The main prompt already tells Codex the whole problem from zero, including the evidence hierarchy and the exact failure mode to investigate.

## How to use the prompts in this file

1. Start with Prompt 1 only.
2. Let Codex take initiative.
3. Use one of the follow-up prompts only if needed.
4. Do not paste all prompts at once.

## Prompt 1 - Main kickoff prompt

```text title="Prompt 1 - Main kickoff"
You are working in a fresh local workspace on a real purchasing research project, not a coding exercise.

Use the workspace proactively. Create scratch files, structured data files, and intermediate notes as needed. Take initiative. Do not wait for hand-holding. However, do not hide uncertainty, and do not force a conclusion that the evidence does not support.

Project goal:
Produce a defensible, evidence-backed shortlist of compact, self-contained wireless speakers available in the UK for under 1000 GBP that are suitable for someone who:
- likes the general form factor of Google Nest Audio
- wants better sound
- wants true Spotify Connect behavior, not merely a generic Google Cast destination
- prioritizes exact Spotify-page confirmation of Lossless 24-bit for the exact model
- treats Google Home / Google Cast compatibility as optional convenience, not the main goal
- wants to minimize the risk of buying a speaker and then discovering at home that Android forces Google Cast instead of native Spotify Connect

Background that matters:
- Current reference point is a Google Nest Audio.
- The user likes the Nest Audio form factor but not its sound quality.
- In the Spotify Android app, Nest Audio appears as a Google Cast destination. The user wants a real Spotify Connect endpoint for the new speaker.
- There is known concern that, on Android, in mixed homes with Google Cast devices present, Spotify may surface Google Cast instead of native Spotify Connect, which could prevent access to a speaker's native 24-bit Spotify Connect path.
- The user has existing Google Home devices, but is willing to stop using them if necessary. Google Home grouping is a convenience only.

Hard constraints:
- Must be a single, self-contained powered speaker.
- Exclude streamers, amps, soundbars, passive speakers, and systems that are not really standalone speakers.
- Must be roughly Google Nest Audio sized: a small tabletop speaker.
- Must be available in the UK.
- Budget cap is 1000 GBP.
- Spotify's own Connect device page for the exact model is the source of truth for Spotify capability.
- The primary target is models that Spotify explicitly marks as supporting Lossless 24-bit over Spotify Connect.

Secondary preferences:
- Bluetooth support is desirable.
- Google Home / Google Cast support is optional and secondary.
- Designed primarily as a standalone speaker.
- Stereo pairing is a bonus, not a requirement.
- Long-term durability and quality matter more than chasing the cheapest option.

Critical evidence hierarchy:
1. Spotify's own exact model page for the exact speaker model
2. Official manufacturer documentation and support articles
3. Recent community evidence from Spotify Community, Reddit, manufacturer forums, and AV forums
4. Retailer listings

Methodology requirements:
- Do not assume Spotify's public Connect site is filterable by 24-bit lossless.
- Investigate whether Spotify's site has any practical systematic way to discover eligible models.
- If not, construct the candidate pool using other sources: manufacturer docs, support pages, product-line pages, press coverage, UK retailer listings, and any other structured public sources.
- Then verify candidate models individually against Spotify's own exact model pages.
- Separate clearly what is confirmed by Spotify, what is confirmed by the manufacturer, and what comes from community reports.
- If a model belongs to another ecosystem, that is acceptable as long as Spotify support is real and there is not a strong pattern of user complaints about Spotify use.
- If evidence is thin or conflicting, say so clearly.
- Do not spend forever chasing perfect automation if a practical browser-based verification path is faster and more reliable.

Very important failure mode to investigate:
- On Android, in mixed Google Cast homes, Spotify may surface Google Cast instead of native Spotify Connect.
- This is NOT a first-pass exclusion filter, because it may otherwise eliminate everything.
- First build the strongest shortlist that satisfies the hardware and Spotify requirements.
- Then do a second-pass risk analysis for Android Cast-vs-Connect behavior using recent community evidence.

Known prior leads that may save time, but must be treated only as leads until verified:
- Denon Home 150 may be only Lossless 16-bit on Spotify's site.
- Denon DNP-2000NE may be Lossless 24-bit on Spotify's site, but it is not a speaker and should therefore be excluded.
- Possible product families worth investigating include compact models from Sonos, JBL Authentics, Bang and Olufsen, Audio Pro, and similar brands.

Expected behavior:
- Create whatever scratch files or structured files you need.
- Keep a running candidate log.
- Keep a running Spotify-verification log.
- Keep a running Android-risk evidence log.
- Be proactive about tool use and browsing.
- Install lightweight tools if useful and permitted.
- Use headless browsing or browser automation if needed for Spotify's JS-heavy site.
- Prefer saving raw evidence before summarizing it.

Deliverables required in the workspace:
1. A final human-readable markdown report.
2. A structured candidate file, such as YAML or JSON.
3. A structured Spotify verification file, model by model.
4. A short notes file listing unresolved questions, conflicting evidence, or any manual validation still recommended.

Required contents of the final report:
- A short answer at the top.
- A strongest shortlist in mobile-friendly narrative form, not a giant table.
- For each shortlisted model, clearly separate:
  1. Whether Spotify's own page confirms Lossless 24-bit for the exact model
  2. Approximate UK price and UK availability
  3. Whether it supports Google Home / Google Cast
  4. Whether it supports Bluetooth
  5. Whether it is genuinely a compact standalone speaker in the right form factor
  6. Community evidence about Android Cast-vs-Connect behavior
  7. Confidence level
  8. Recommendation category such as Strong fit, Promising but risky, Fallback, or Avoid
- A section of notable models excluded and why.
- A section explaining what the Android risk actually seems to be.
- A section on best next validation steps before purchase.

Output style requirements for the final report:
- Mobile-friendly narrative format.
- No giant tables unless absolutely necessary.
- Keep caveats visible.
- Be decisive where evidence is strong.
- Be explicit where evidence is weak.

Begin by planning your own approach, setting up your workspace artifacts, and then executing the research.
```

## Prompt 2 - If Codex starts over-focusing on one subproblem

Use this only if Codex gets stuck on Spotify scraping, a single brand, or a single page.

```text title="Prompt 2 - Rebalance and continue"
Rebalance the project.

Do not get stuck on any one website or model.

Continue from the existing workspace state and optimize for overall progress:
- keep building the candidate pool
- keep excluding obvious non-matches
- keep verifying Spotify model pages where practical
- keep gathering Android Cast-vs-Connect risk evidence
- keep the structured files up to date

If Spotify page extraction is becoming a bottleneck, use a pragmatic fallback:
- verify as many models as you can directly
- clearly log which exact-model Spotify checks remain unresolved
- continue the rest of the project instead of stalling

Then finish the report with confidence labels and explicit unresolved items.
```

## Prompt 3 - If you want to force a Spotify-only verification pass

Use this if the general research is done but the Spotify exact-model verification still needs tightening.

```text title="Prompt 3 - Spotify verification only"
Do a focused Spotify-verification pass only.

Continue from the existing workspace and do not redo the broad product research.

Your goal in this pass is to improve the exact-model Spotify evidence for the current candidate list.
For each candidate model still under consideration:
- locate the exact Spotify Connect page for the exact model if possible
- extract the feature pills or equivalent labels shown on Spotify's page
- record whether Spotify explicitly confirms Lossless 24-bit, Lossless 16-bit, Bluetooth, WiFi, Multiroom, Works with Spotify Free, and any other relevant labels shown
- save this evidence into the structured Spotify verification file
- if a page is missing, ambiguous, region-blocked, or not machine-readable, log that clearly rather than guessing

Do not drift into general review reading unless it directly helps resolve the Spotify page for a candidate.
```

## Prompt 4 - If you want a final polish pass on the report only

Use this if Codex has already done the research and you only want a cleaner final deliverable.

```text title="Prompt 4 - Final report polish"
Polish the final report only.

Do not do major new research unless a tiny missing fact is blocking clarity.
Use the existing workspace evidence.

Requirements:
- keep it mobile-friendly
- no giant tables
- keep Spotify-confirmed facts clearly separated from manufacturer-confirmed facts and community-reported facts
- keep confidence levels and caveats visible
- make the shortlist easy to read on a phone
- make the buying recommendation practical rather than abstract

Also produce a short companion summary that says, in plain English, which 2 or 3 models should be checked first and why.
```

## Final note for you

If Codex is behaving well, Prompt 1 may be enough by itself.

The follow-up prompts exist to steer, not to replace the initial brief.
