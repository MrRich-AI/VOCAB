# VOCAB builds — rules for Claude Code

This repo holds Mr. Rich's VOCAB builds: vocabulary decks converted from pptx into self-contained, interactive HTML for Grade 9 and 10 IGCSE ESL students in Vietnam.

These rules are kept in sync with the "CONVERT | VOCAB | BASIC HTML Builds" Project on claude.ai. When a rule is added or changed in either place, it is copied to the other.

## General working rules
- If a request seems to contradict or clash with these rules, ask before building anything.
- Never commit API keys or secrets.
- Ask before committing and pushing a new or changed build.

## Repo layout
- One folder per unit: `unit-N/index.html` (one self-contained HTML file) plus `unit-N/thumb.jpg` (landing-page thumbnail, usually from the deck's title slide).
- The root `index.html` is the landing page. Its `BUILDS` array is edited by hand: add an entry for each new unit with `folder`, `title` ("Unit N Vocabulary"), `group` ("Unit N"), `desc` (topic summary and term count) and `tags` (term count, card modes, games).
- Chinese versions live in the same file as the Vietnamese one (see below), so they never get a new folder or a landing-page entry.

## What a VOCAB build is
- A build type that starts from the BASIC rules (below). The build looks identical to the source pptx.
- Sources are vocabulary decks, not tests with answer keys. Each card has a term, part of speech, definition, example sentence, Vietnamese translation and picture.
- The slides can be presented in several different ways.
- Students use the build on their own devices and can edit their slides. They save by downloading an edited copy of the HTML ("save as a new file").

## Base rules inherited from BASIC
- Read the whole source before building: every slide, speaker notes (context only, never shown), hidden slides only if relevant.
- Ask if the title or Unit number is unclear.
- Match the source's colours, fonts, sizes, backgrounds, images, look, wording and order. If a font has to be substituted, use the closest match and say so.
- Extract media at original resolution and embed it as base64. Rebuild text and tables as real HTML; use a rendered image only for elements that can't be matched.
- Links stay clickable. Small audio/video is embedded; ask about large or online-only media. Flag anything that won't work offline.
- **Override:** typos and similar mistakes in the source (e.g. a wrong pronoun) are always fixed without asking; just say the change was made. (BASIC keeps typos; VOCAB does not.)

## Layout
- Always prioritize the laptop (16:9) layout.
- On phones, reformat to widescreen when the phone is turned sideways. Small text size and typing on phones use the previously agreed phone handling.
- No flag emojis anywhere (they show as letters like "GB"/"VN" on Windows). Use plain text or a non-flag icon instead.

## Start screen
- Styled like the deck's first/title slide.
- Asks for name and class. These are shown on students' saved files. Nothing is submitted to a Google Sheet.

## Cards menu
- **Mr. Rich's Cards:** the deck as made. This button glows and wobbles, with a "START HERE" starburst.
- **Flashcard Flip:** listed under Mr. Rich's Cards (details below).
- **Add Term:** term and example sentence removed; students add the term and an optional sentence.
- **Add Definition:** definition and Vietnamese removed; students add the definition and optional Vietnamese.
- **Add Everything:** all text removed; the picture stays.
- **Blank:** picture and all text except the term removed; students can add text and pictures if they like.
- Choosing any Cards option (except Flashcard Flip) shows a "Shuffle Cards?" prompt: yes shuffles the card order, no keeps the original order.

## Flashcard Flip
- True flash-card mode with an animated flip. Students mark each card "correct" or "study again".
- One side has the definition (no example sentence); the other has the term.
- Two versions, chosen in a popup window: (a) English with Vietnamese (Chinese in ?zh builds), (b) English only.
- Defaults to definition side first, with a button to switch to term first.
- The picture goes on whichever side the student sees first (default: definition side).
- Always shuffled; no "Shuffle Cards?" prompt.
- "Study again" cards come back in another round until all are correct, with an option to end and show the score instead.

## Word family
- A "Word family" button on each card opens a window showing each form with its part of speech highlighted, a definition where it differs from the original form, an example sentence, and the Vietnamese (or Chinese in ?zh builds) translation. No picture.
- The original word is in the first row at the top.
- The window background can be the faded title slide.
- Aim for every word unless it has no useful form; ask if unsure. Words with no useful or only marginal forms get no button (e.g. Unit 3: Outlets, Busy, Cosy, Delicious were left out).
- The button appears in Mr. Rich's Cards and Make Your Own only.

## GAMES menu
- A separate "GAMES" menu with Picture Match, Gap-Fill Sentences, Vietnamese → English, a speed review, and Spell It.
- The speed review flashes the definition (not a picture) and students choose the term.
- In Picture Match, clicking a picture enlarges it.
- Games are just practice: no submission.
- After seeing a new source pptx, suggest a few extra activities.
- **Unique games:** for every new build, suggest 3 unique games tied to the unit's theme. Their formats must not duplicate the standard games above, Falling Words, or any unit-specific game already in the repo (Verb Patterns, Penalty Shootout, File Manager, Memory Feast, Expedition Crossword, Notice Board Word Search, Odd One Out).
- **Unique-game rollout (approved, not yet built):** Unit 1 Penalty Shootout (shoot left if the term is used correctly, right if misused), Unit 2 File Manager (drag words into part-of-speech folders), Unit 3 Memory Feast (term–picture concentration on plates), Unit 11 Expedition Crossword (map-style, definitions as clues), Unit 12 Notice Board Word Search (definition clues), Unit 13 Odd One Out (all 26 words, with a reason after each pick). The new games work with the `?zh` link in Units 1–3. In the same pass, replace the flag emoji on the Vietnamese → English button in Units 1, 2, 11 and 12.

## Example sentences
- New example sentences connect to Vietnamese culture rather than the grammar lessons.
- They must use the term in the same part of speech the card gives.
- Include word forms too.
- Grammar (Language Focus) gets its own separate builds in the future, not in VOCAB builds.

## Chinese versions (Units 1–10)
- Replace all Vietnamese with simplified Chinese (no pinyin) in all cards and games. Translate from the English, never from the Vietnamese. The Chinese covers the same English item the Vietnamese translates on each card.
- Built from each unit's existing Vietnamese VOCAB build.
- All buttons and instructions stay in English. Device fonts for Chinese are fine (no embedded font). No separate translation check before building.
- One file per unit holds both languages: the normal link is Vietnamese and the `?zh` link is Chinese. Update the existing unit file rather than adding a new one.
- The language is set only by the link (no on-screen toggle). Downloaded edited copies remember their language.
- No change to the landing page.
- Units 11 and up have no ?zh version.

## Rollout of newer features
- Flashcard Flip, Word family and part-of-speech-matched sentences go into new builds first.
- Done so far: Unit 3 (with its ?zh Chinese version) and Unit 13 (no ?zh).

## Before delivering
- Check at 1920×1080 (inherited from BASIC): no overflow, each card compared with the source.
- Give a short report: typos fixed, font substitutions and anything not reproduced exactly.
