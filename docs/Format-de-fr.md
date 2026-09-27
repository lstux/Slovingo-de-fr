# Format Slovingo-de-fr

## Overview

This document describes how content is structured in Slovingo-de-fr, specifically its adaptations for children compared to the adult-focused format used in other Slovingo courses.

The foundation is **SMD (Slovingo Markdown)** — see the [main Slovingo docs](https://github.com/lstux/Slovingo/tree/main/docs) for the complete technical reference.

## Adaptations for Kids

### 1. Lighter, more playful tone

**Adult (sk-fr, fr-sk):**
> Doslova „dobrý deň". Môžeš ho použiť v každej situácii, kde nepoznáš osobu.
> (Literally "good day". You can use it in any situation where you don't know the person.)

**Kids (de-fr):**
- Shorter sentences
- More exclamation marks and emojis
- Explanations tied to everyday scenarios kids experience
- Sometimes informal, like talking to a friend

### 2. Visual & interactive elements

- **More illustrations**: Every fiche gets a vivid, engaging image (kids, animals, activities)
- **Emoji markers**: More liberal use of emojis for characters, emotions, and themes
- **Varied exercises**: Not just "hear and translate" — matching, true/false, role-play prompts
- **Gamification ready**: Structure supports stars, badges, streak tracking

### 3. Series progression

While we keep the **intro/series/vocabulary/annex** structure from adult courses, each series targets:

- **4 fiches** (not 5): Core vocabulary only, shorter lessons
- **1 dialogue fiche**: Playful conversation (not a full mini-story)
- **1 extra fiche**: Vocabulary recap + exercise foundation

This makes learning more manageable for kids with shorter attention spans.

### 4. Character-driven dialogues

Kids engage better with recurring characters:
- A protagonist kid (gender-neutral or varying)
- A friendly adult (parent, teacher, grandparent)
- Maybe a pet 🐶

Dialogues replay the series vocabulary in fun contexts: asking for help, getting lost, ordering food, etc.

---

## File structure

```
slovingo-de-fr/md/
├── 00_Introduction_*.md          # Intro fiches (how to use, alphabet, sounds, etc.)
├── 10_Series_XX_Theme_YY_*.md    # Learning series
├── 20_Vocabulary_*.md            # Standalone vocab lists (by topic or level)
└── 30_Annex_*.md                 # Cultural notes, grammar tables, etc.
```

### Series numbering

- **Series 00**: Kit de Survie (survival phrases)
- **Series 01+**: Thematic progressions (Familie, Haus, Essen, etc.)

Example filename: `10_Series_01_Familie_02_das-zuhause.md`

---

## Fiche structure

### Introduction fiches (00_Introduction_*)

- Quick, friendly intro to the course
- Alphabet + pronunciation (German sounds for French speakers)
- Counting (0-10, then 10-100)
- No lengthy explanations — link to Slovingo main docs if details needed

### Series fiches (10_Series_XX_*)

**Fiches 01-04: Learning fiches**

```markdown
# Series NAME (X/Y) — Deutsch titel

@ img/theme.jpg | Picture caption with source

Short, friendly intro (1-2 sentences, not a paragraph).

---

## Die neuen Wörter

| Deutsch | Français |
|---------|----------|
| Hallo | Bonjour |
| ... | ... |

(~7 essential words)

---

## Heute lernen wir...

### A grammar point

Short explanation in French, tied to the words above.

| Deutsch | Français |
|---------|----------|
| Ich heiße Anna. | Je m'appelle Anna. |
| ... | ... |

---

## Sätze (Sentences)

! Hallo!
> Bonjour !
> Hallo = bonjour
+ Informal greeting, with friends or family.

(6-8 audio cards, progressively building)

---

## Das wiederholen wir (We review)

(From series 02 onward: reuse words from previous fiches)

---

## 🇩🇪 German corner

2-3 short paragraphs about German culture tied to the theme.
Use {{speakable}} for key words.

---

## Mehr Wörter (Extra words)

| Deutsch | Français |
|---------|----------|
| ... | ... |

(~7 additional/complementary words)

---

## Noch mehr Sätze (More sentences)

(3-5 audio cards with complementary vocab)
```

**Fiche 05: Dialogue**

- Mini-story or extended dialogue with recurring characters
- Reuses all vocabulary from fiches 01-04
- No new words (or marked with "new word!" if essential)
- 8-12 audio cards as a continuous exchange

**Fiche 06: Extra**

- Complete vocabulary table for the series
- 15-20 audio cards mixing series vocab freely
- Used as raw material for exercises
- No new learning — pure review and reuse

---

## Audio cards in practice

### Basic structure

```
! Wie heißt du?
> Comment t'appelles-tu ?
> Wie heißt du = comment t'appelles-tu
+ "du" = you (informal)
```

### With speaker markers (dialogues)

```
👦 ! Hallo, ich bin Tom.
> Salut, je m'appelle Tom.

👩 ! Hallo Tom! Wie geht's?
> Salut Tom ! Ça va ?
```

### With cultural notes

```
! Guten Morgen!
> Bonjour ! (Good morning)
+ Very formal. Used with teachers, strangers, etc.
```

---

## Illustrations

Every fiche header has an illustration:

```markdown
@ img/theme-name.jpg | Caption: child doing X, or Y object. Source: Wikimedia Commons
```

**Guidelines:**
- Child-friendly, diverse, and joyful
- From Wikimedia Commons (free license) or commissioned
- ~600-800px wide, clear and engaging
- Captions include source and license

---

## Language notes (Coin Allemand)

Keep these light and fun:

✅ **"Did you know? Germans have a word for..."**
✅ **"In German, people say... when they mean..."**
✅ **"Fun fact: [cultural tidbit] is super important in Germany"**

❌ Don't: Assume advanced grammar knowledge
❌ Don't: Be overly formal or academic

---

## Vocabulary lists (20_Vocabulary_*)

Standalone reference docs:

- Organized by topic (Farben = colors, Tiere = animals)
- Or by level (A1, A2, A3)
- Simple tables: Deutsch | Français | Lautschrift (phonetic guide)
- No audio cards

---

## Annex (30_Annex_*)

Grammar tables, conjugation, gender rules, etc.:

- Reference material (not for learning)
- Can be dry/academic since it's supporting, not primary
- Linked from series fiches where relevant

---

## Translation quality

- Français: Natural French for a kid (~8-12 years old), not overly formal
- Deutsch: Common, practical German for learners
- Avoid idioms that don't translate; use explanations instead

---

## Progress tracking

All content files follow the naming scheme so the build system can automatically:
- Detect category and ordering
- Generate navigation
- Assign exercises to practice material
- Build the table of contents

See [../lang.json](../lang.json) and the main Slovingo docs for implementation details.

---

## Quick checklist before publishing a fiche

- [ ] Illustration is clear, kid-friendly, diverse
- [ ] Vocabulary is cumulative (reuses previous fiches)
- [ ] Grammar explanations are 1-2 sentences max
- [ ] Audio cards are playable (no unknown vocab)
- [ ] Character dialogue feels natural (not textbook-y)
- [ ] German corner is ~3 short paragraphs (culture, not grammar)
- [ ] Extra fiche (06) has no new words
- [ ] All filenames follow the scheme
- [ ] Tone is encouraging, not intimidating

---

## Next steps

1. Build first series (Kit de Survie)
2. Collect feedback from kid testing
3. Iterate on tone, pacing, illustrations
4. Add exercises once series 0-1 are stable
5. Explore code adaptations (gamification, UI tweaks) as needed
