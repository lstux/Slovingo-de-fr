# Slovingo-de-fr Documentation

Welcome! This folder contains the guides for understanding and contributing to the Slovingo-de-fr project.

## 📖 Start here

**New to the project?**
- Read [../README.md](../README.md) first for the big picture
- Then come back here for details

**Want to write content (fiches)?**
- Start with **[Format-de-fr.md](./Format-de-fr.md)** — explains how to structure fiches and use the SMD format
- Check **[Progression.md](./Progression.md)** — understand the learning journey and what to teach when

**Want to understand the learning approach?**
- See **[Progression.md](./Progression.md)** — pedagogical philosophy and series structure

**Need technical details?**
- Refer to the **[main Slovingo docs](https://github.com/lstux/Slovingo/tree/main/docs)** for:
  - Complete SMD format reference (Format-SMD.txt)
  - Build pipeline and CI (CI-Pipeline.md)
  - File naming conventions (Fiches-Serie.txt)

## 📁 Files in this folder

| File | Purpose |
|------|---------|
| **Format-de-fr.md** | How to write fiches for kids — structure, tone, examples |
| **Progression.md** | Learning roadmap — what to teach, in what order, why |
| **README.md** | You are here! |

## 🚀 Quick workflow

### To write a new fiche:

1. Decide which series and fiche number (e.g., Series 01, fiche 02)
2. Open **[Format-de-fr.md](./Format-de-fr.md)** to see the template
3. Write your fiche in `/md/` following the naming scheme
4. Add an illustration to `/img/`
5. Commit and push to the repo

### To add exercises:

1. Write the fiche first (fiches 01-04 need to be stable)
2. Use the "extra" fiche (06) as your exercise base
3. Generate JSON exercises (see main Slovingo docs)
4. Add to `/exercises/`

### To iterate on pedagogy:

1. Test fiches with kids
2. Document what works/doesn't in an issue or PR comment
3. Refine tone, pacing, vocab as needed
4. Update this doc if the approach changes

## 🔗 Related documentation

- **[Slovingo main repo](https://github.com/lstux/Slovingo)** → Technical framework, code, build system
- **[Format-SMD.txt](https://github.com/lstux/Slovingo/blob/main/docs/Format-SMD.txt)** → Complete SMD format (we use it here)
- **[Fiches-Serie.txt](https://github.com/lstux/Slovingo/blob/main/docs/Fiches-Serie.txt)** → Adult series structure (we adapt it for kids)

## 💡 Design principles

The format and progression documents are built on these core ideas:

1. **Kids learn through play** — tone is light, structure is clear
2. **Progress is visible** — series complete in ~1 week, fiches in ~1 day
3. **Repetition works** — vocabulary is reused, reinforced, deepened
4. **Culture matters** — kids want to know *why* they're learning German
5. **Flexibility rules** — adapt format and code as real testing shows what works

## ❓ Questions?

- **About the pedagogical approach?** → Check [Progression.md](./Progression.md)
- **About fiche format and writing?** → Read [Format-de-fr.md](./Format-de-fr.md)
- **About SMD syntax or build system?** → See [Slovingo main docs](https://github.com/lstux/Slovingo/tree/main/docs)
- **Got feedback or ideas?** → Open an issue or submit a PR!

---

**Status:** 🚀 Documentation is evolving alongside content. Check back as we add more fiches and learn what works!
