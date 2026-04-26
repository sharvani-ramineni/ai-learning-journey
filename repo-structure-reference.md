# Final Repo Structure — Reference

---

## PUBLIC REPO: `ai-learning-journey`

```
ai-learning-journey/
├── README.md
├── content-log.md
├── month-1-plan.md                          ← public version (no resources)
│
├── week-01-llm-fundamentals/
│   ├── day-01-tokenization/
│   │   ├── notebook.ipynb                   ← your Colab notebook
│   │   ├── NOTES.md                         ← your technical write-up
│   │   └── resources.md                     ← links used + your Medium/Substack URLs
│   ├── day-02-embeddings/
│   │   ├── notebook.ipynb
│   │   ├── NOTES.md
│   │   └── resources.md
│   ├── day-03-attention-part1/
│   │   └── ...
│   ├── day-04-attention-part2/
│   │   └── ...
│   ├── day-05-sampling/
│   │   └── ...
│   └── day-06-bigram-model/
│       └── ...
│
├── week-02-building-gpt-and-scale/
│   └── (same day structure)
├── week-03-working-with-llm-apis/
│   └── (same day structure)
├── week-04-first-real-agent/
│   └── (same day structure)
│
│   LOCAL ONLY (excluded via .git/info/exclude — never on GitHub):
├── templates/
├── setup.sh
├── fix-missing-templates.sh
├── START-HERE.md
├── claude-project-setup.md
└── github-profile-readme.md
```

### What goes in each file:

**notebook.ipynb** — Your Colab code. Saved via File → Save a copy in GitHub.

**NOTES.md** — Your technical write-up. Filled from template. Contains:
- What this concept is (in your own words)
- Why it matters
- The key insight that surprised you
- What you built + how to run it (exact bash/pip commands)
- Where you got stuck + what fixed it
- Technical details worth remembering (formulas, gotchas, API quirks)
- Questions you still have
- Connections to earlier days
- Links to your Medium + Substack posts (added after Sunday publishing)

**resources.md** — Links you used:
- Primary source
- Extra perspectives explored
- Your own Medium + Substack URLs (added after Sunday)
- What you'd read next to go deeper

---

## PRIVATE REPO: `ai-content-drafts`

```
ai-content-drafts/
├── README.md
├── START-HERE.md
├── claude-project-setup.md
├── github-profile-readme.md
├── month-1-plan-private.md                  ← full plan with all resources
├── repo-structure-reference.md              ← this file
│
├── _templates/
│   ├── medium_TEMPLATE.md
│   ├── substack_TEMPLATE.md
│   ├── linkedin_TEMPLATE.md
│   ├── instagram_TEMPLATE.md
│   ├── raw_notes_TEMPLATE.md
│   └── README_CONTENT.md
│
├── week-01-llm-fundamentals/
│   ├── day-01-raw.md                        ← your messy raw notes for day 1
│   ├── day-02-raw.md                        ← your messy raw notes for day 2
│   ├── day-03-raw.md
│   ├── day-04-raw.md
│   ├── day-05-raw.md
│   ├── day-06-raw.md
│   ├── medium.md                            ← weekly Medium deep-dive
│   ├── substack.md                          ← weekly Substack teaser
│   ├── linkedin.md                          ← weekly LinkedIn post
│   └── instagram.md                         ← weekly reel script
│
├── week-02-building-gpt-and-scale/
│   ├── day-01-raw.md through day-06-raw.md
│   ├── medium.md
│   ├── substack.md
│   ├── linkedin.md
│   └── instagram.md
│
├── week-03-working-with-llm-apis/
│   └── ...
└── week-04-first-real-agent/
    └── ...
```

**Raw notes are daily (your messy thinking). Content files are weekly (Claude-generated).**

---

## CLAUDE PROJECT: "AI Learning Journey"

**Custom Instructions:** System prompt from `claude-project-setup.md`

**Project Knowledge (uploaded files):**
- `month-1-plan-private.md`
- `medium_TEMPLATE.md`
- `substack_TEMPLATE.md`
- `linkedin_TEMPLATE.md`
- `instagram_TEMPLATE.md`
- (ongoing) each day's `NOTES.md` as you write them

---

## Your exact daily flow

### Weekday — 60 min learning + 15 min notes validation

```
MORNING (5 min)
│
├─ Open Claude Project
├─ Type: "Starting Day X — [topic]"
├─ Read the orientation (5 sentences + what to watch for)
│
LEARNING (50 min)
│
├─ Watch/read primary resource (25 min)
├─ Code in Colab (25 min)
│
WRAP UP — RAW NOTES (5 min)
│
├─ Colab → File → Save a copy in GitHub
│     path: week-XX-name/day-XX-topic/notebook.ipynb
├─ Open day-XX-raw.md in PRIVATE repo (from template)
├─ Brain dump: what you think you understood, what confused you,
│     what surprised you, code that broke, questions
├─ Write fast and messy — this is for you, not readers
│
VALIDATION WITH CLAUDE (10-15 min)
│
├─ Paste raw notes into Claude Project:
│     "Check my understanding for Day X"
├─ Claude validates: what's correct, what's wrong, what's missing
├─ You ask follow-ups, push back, rewrite if needed
├─ Iterate until you both agree your understanding is solid
│
├─ When ready, say: "Format for public"
├─ Claude outputs a clean NOTES.md in the public template format
├─ Copy that output → paste into NOTES.md in PUBLIC repo day folder
├─ git add . && git commit -m "day X: topic" && git push (public)
├─ git add . && git commit -m "day X raw notes" && git push (private)
│
DONE. Close laptop.
```

### Saturday — 3 hrs (build session)

```
├─ Build the week's project or catch up on missed days
├─ Commit + push
├─ No content work
```

### Sunday — 90 min (review + content)

```
STEP 1: KNOWLEDGE CHECK (30 min)
│
├─ Open Claude Project
├─ Paste all 5-6 NOTES.md files from the week
├─ Type: "End of week X check. Ask me the hardest questions."
├─ Answer them — this is your revision
├─ If Claude says you have gaps, revisit before next week
│
STEP 2: CONTENT GENERATION (60 min)
│
├─ Type: "Week X done, generate content."
├─ Claude outputs 4 sections:
│     --- MEDIUM ---
│     --- SUBSTACK ---
│     --- LINKEDIN ---
│     --- INSTAGRAM REEL SCRIPT ---
│
├─ Copy MEDIUM output → private repo week-XX/medium.md
│     → skim 5 min → publish to Medium
│
├─ Copy SUBSTACK output → private repo week-XX/substack.md
│     → skim 2 min → publish to Substack
│
├─ Copy LINKEDIN output → private repo week-XX/linkedin.md
│     → skim 2 min → publish to LinkedIn
│
├─ Copy INSTAGRAM output → private repo week-XX/instagram.md
│     → read script aloud once → record reel (one take)
│
├─ Go back to PUBLIC repo:
│     → Update each day's resources.md with published Medium/Substack URLs
│     → Update content-log.md
│     → git add . && git commit -m "week X: add content links" && git push
│
├─ PRIVATE repo:
│     → git add . && git commit -m "week X content published" && git push
│
DONE.
```
