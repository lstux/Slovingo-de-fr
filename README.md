# Slovingo-de-fr 🇩🇪 🇫🇷

🌐 **Le cours en ligne : [lstux.github.io/slovingo-de-fr-kids](https://lstux.github.io/slovingo-de-fr-kids/)**

**Apprendre l'allemand de manière ludique — pour les enfants à partir de 8 ans**

Un cours d'allemand construit sur le framework [Slovingo](https://github.com/lstux/Slovingo), conçu spécialement pour les enfants francophones.

L'app s'appelle **Fuchsbau**, « le terrier du renard » en allemand : le coin où le renard 🦊 (toi) retrouve Lea 🐰, un lièvre de la Forêt-Noire, pour apprendre. Voir [docs/Format-animaux.md](docs/Format-animaux.md).

## 📚 Qu'est-ce qu'il y a dedans ?

- **Fiches** : cartes interactives avec prononciation et audio
- **Séries** : progressions thématiques avec difficulté croissante
- **Dialogues** : conversations avec des personnages récurrents
- **Exercices** : activités variées pour pratiquer et consolider
- **Vocabulaire** : listes de mots organisées par thème

## ✨ Qu'est-ce qui rend ce cours particulier ?

Ce cours est conçu **pour les enfants, par l'expérimentation**. On adapte le format d'apprentissage éprouvé de Slovingo (pensé initialement pour des adultes) pour le rendre :
- **Moins formel** : introductions légères, sans jargon
- **Plus interactif** : éléments ludiques, exercices variés
- **Visuellement engageant** : illustrations, emojis, personnages
- **Flexible** : le format et même le code de Slovingo peuvent évoluer si besoin

## 🚀 Pour commencer

1. **Le dossier [docs](./docs/)** contient les guides de format et l'approche pédagogique
2. **[docs/Progression.md](./docs/Progression.md)** détaille la progression d'apprentissage
3. **[docs/Format-de-fr.md](./docs/Format-de-fr.md)** explique comment le contenu est structuré

## 📂 Structure du projet

```
slovingo-de-fr/
├── docs/                 # Documentation du projet
├── md/                   # Contenu des fiches (format Slovingo Markdown / SMD)
├── exercises/            # Définitions des exercices (JSON)
├── img/                  # Illustrations et ressources
└── lang.json             # Configuration de la langue (allemand → français)
```

## 🔗 Dépôts liés

- **[lstux/Slovingo](https://github.com/lstux/Slovingo)** — le framework principal (code, moteur de génération, docs)
- **[lstux/Slovingo-fr-sk](https://github.com/lstux/Slovingo-fr-sk)** — cours français→slovaque (référence adulte)
- **[lstux/Slovingo-sk-fr](https://github.com/lstux/Slovingo-sk-fr)** — cours slovaque→français (référence adulte)
- **[lstux/Slovingo-bzh-fr](https://github.com/lstux/Slovingo-bzh-fr)** — cours breton→français

## 📝 Format

On utilise le **SMD (Slovingo Markdown)**, une extension légère et lisible du Markdown :

- **Cartes audio** avec traduction et explications
- **Tableaux de traduction** pour le vocabulaire
- **Éléments prononçables** `{{mot}}` pour la synthèse vocale
- **Illustrations** avec légende
- **Dialogues** avec marqueur de locuteur (emoji)

Voir [docs/Format-de-fr.md](./docs/Format-de-fr.md) pour le détail de nos adaptations, et la [documentation Slovingo](https://github.com/lstux/Slovingo/tree/main/docs) pour la référence technique complète (syntaxe SMD, pipeline de build).

## 👨‍👧 Qui est derrière ce projet ?

Projet familial : mon fils (8 ans) est le cobaye principal. Le format et le contenu sont donc amenés à évoluer selon ce qui fonctionne vraiment avec lui, plutôt que de suivre à la lettre un plan pédagogique théorique.

---

**Statut** : ✍️ Introduction, Kit de Survie et 6 séries écrites (Familie, Haus, Essen, Stadt, Tiere, Spiele — 45 fiches), dans le monde des animaux de la Forêt-Noire (branche `animals`, voir [docs/Format-animaux.md](docs/Format-animaux.md)). À venir : illustrations (photos réelles d'animaux et de paysages), séries suivantes.

## 🌐 Déploiement (GitHub Pages)

À chaque push sur `main`, le workflow `.github/workflows/pages.yml` construit le site avec le moteur [Slovingo](https://github.com/lstux/Slovingo) et le publie sur **https://lstux.github.io/slovingo-de-fr-kids/**. L'`url_path` est adapté au moment du build (sans modifier `lang.json` dans le repo).

Réglage à faire **une seule fois** : *Settings → Pages → Build and deployment → Source : GitHub Actions*.

Le workflow `build-release.yml` (release tarball, à lancer à la main) reste en place.

---

*Slovingo est libre et open-source, sous licence [GPL-3.0](./LICENSE).*
