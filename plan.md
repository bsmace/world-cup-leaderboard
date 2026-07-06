# Implementation Plan

## Steps

### 1. DATA — Extract & build data.json
- Python script reads both sheets (Group Stages + Round of 32) from xlsx
- Merges per player: chit#, name, combined pair, team1_gs, team2_gs, team1_r32, team2_r32, total
- Outputs clean `data.json`
- Run once, commit alongside HTML

### 2. UI — Build index.html
Single self-contained file (CSS + JS inline):
- **Structure**: hero → podium (1st-3rd) → tier cards (4th-6th) → honorable mentions grid
- **Glassmorphism CSS**: `backdrop-filter: blur()`, rgba borders, gold/teal gradients
- **Search**: real-time filter by name or nation
- **Animations**: count-up on scroll (IntersectionObserver), confetti on champion, fade-in cards
- **Modals**: player detail on click (breakdown, flags, rank)
- **Responsive**: mobile-first, stack tiers vertically on small screens
- **Flags**: inline emoji + CSS-based flag sprites

### 3. INTEGRATION — Wire data.json into UI
- `<script>` tag loads `data.json`
- JavaScript generates all DOM from data

### 4. VERIFY
- Manual viewport testing (mobile 375px → desktop 1440px)
- Confirm all 91 players render
- Confirm sort order: points desc → name asc for ties
- Confirm search works

### 5. DEPLOY
- `git init` → `git add` → `git commit`
- `vercel --prod` or connect GitHub repo to Vercel
