# Format Slovingo-de-fr

## Vue d'ensemble

Ce document décrit comment le contenu est structuré dans Slovingo-de-fr, en particulier les adaptations faites pour des enfants (8-12 ans) par rapport au format destiné aux adultes des autres cours Slovingo.

La base reste le **SMD (Slovingo Markdown)** — voir la [documentation Slovingo](https://github.com/lstux/Slovingo/tree/main/docs) (`Format-SMD.txt`) pour la référence technique complète.

## Adaptations pour les enfants

### 1. Un ton plus léger, plus ludique

**Cours adulte (sk-fr, fr-sk) :**
> Doslova „dobrý deň". Môžeš ho použiť v každej situácii, kde nepoznáš osobu.
> (Littéralement « bonne journée ». Tu peux l'utiliser dans toute situation où tu ne connais pas la personne.)

**Cours enfant (de-fr) :**
- Phrases plus courtes
- Plus de points d'exclamation et d'emojis
- Explications rattachées à des situations concrètes du quotidien d'un enfant (école, goûter, aire de jeux, argent de poche…)
- Ton parfois familier, comme si on parlait à un copain

### 2. Des éléments visuels et interactifs

- **Plus d'illustrations** : chaque fiche a une image vivante et engageante (enfants, animaux, activités)
- **Marqueurs emoji** : usage plus généreux pour les personnages, les émotions, les thèmes
- **Exercices variés** : pas seulement « écoute et traduis » — appariement, vrai/faux, mise en situation
- **Prêt pour la gamification** : la structure permet d'ajouter étoiles, badges, séries de jours consécutifs

### 3. Une série = 6 fiches

On garde la structure **intro / séries / vocabulaire / annexes** des cours adultes. Chaque série compte :

- **4 fiches d'apprentissage** (01 à 04) : un thème, un ou deux points de grammaire
- **1 fiche dialogue** (05) : une scène avec les personnages récurrents
- **1 fiche extra** (06) : récapitulatif du vocabulaire + base pour les exercices

Exception : le **Kit de Survie** (série 00) n'a que 3 fiches + l'extra.

### 4. Des dialogues portés par des personnages — et par l'enfant lui-même

Les personnages récurrents (tous avec une tête d'animal comme avatar) sont décrits dans [Progression.md](./Progression.md#personnages-récurrents) : 🦊 l'enfant lui-même, 🐰 Lea, 🐨 Tom, 🦉 Oma Hilde.

Les dialogues remobilisent le vocabulaire de la série dans des situations concrètes : se présenter, jouer à cache-cache, déjeuner chez Oma, se perdre en ville, aller au zoo, soirée jeux…

**Le protagoniste, c'est l'enfant lui-même.** Slovingo fournit un mécanisme intégré pour ça (déjà utilisé dans le cours sk-fr) :

- **`[ASK_USER_NAME]`** : insère un champ de saisie directement dans le texte (ex. `Ich heiße [ASK_USER_NAME].`)
- **`[USER_NAME]`** : réutilise ensuite ce prénom partout où on veut personnaliser (ex. `Freut mich, [USER_NAME]!`)
- **Emoji du locuteur : `🦊`** — une tête d'animal plutôt qu'une silhouette humaine : plus ludique, et ça évite d'avoir à choisir un genre.

**On le demande dès la première fiche.** `[ASK_USER_NAME]` apparaît une première fois tout au début de `00_Introduction_01_les-pays.md`, en français, avant tout contenu en allemand — comme la navigation n'est pas strictement linéaire (menu par catégories), un enfant peut atterrir sur n'importe quelle fiche en premier, et sans ça il verrait le nom de secours (`site.user_name_default`, ex. « Enfant ») dans les dialogues des séries. Le champ réapparaît ensuite dans le Kit de Survie (fiche 3, `Ich heiße [ASK_USER_NAME]`) et dans Familie (fiche 5), cette fois lié à la phrase allemande correspondante (« wie heißt du / ich heiße ») — il est alors pré-rempli avec le prénom déjà saisi, donc sans redemander vraiment.

Le nom de secours (si l'enfant n'a rien saisi) vient de `lang.json` → `site.user_name_default`, et le texte du champ de `site.user_name_placeholder`. Dans les exercices, les deux marqueurs sont remplacés par le prénom (résolu par [lstux/Slovingo#13](https://github.com/lstux/Slovingo/pull/13), fusionnée) : on peut donc les utiliser aussi dans les fiches extra.

---

## Structure des fichiers

```
slovingo-de-fr/md/
├── 00_Introduction_*.md          # Fiches d'intro (pays, langue, prononciation, nombres)
├── 10_Series_XX_Theme_YY_*.md    # Séries d'apprentissage
├── 20_Vocabulary_*.md            # Listes de vocabulaire autonomes (par thème ou niveau)
└── 30_Annex_*.md                 # Notes culturelles, tableaux de grammaire, etc.
```

### Numérotation des séries

- **Série 00** : Kit de Survie (phrases de base)
- **Série 01+** : progressions thématiques (Familie, Haus, Essen, Stadt, Tiere, Spiele…)

Exemple de nom de fichier : `10_Series_01_Familie_02_wie-alt-bist-du.md`

Le « thème » du nom de fichier (`Familie`, `KitSurvie`…) donne la clé de sous-groupe dans `lang.json` → `subgroups`, **en minuscules et sans préfixe** (`"familie": "Familie"`).

### Titres

- Fiches 01 à 05 : `# Série Familie (2/5) — Wie alt bist du?`
- Fiche 06 : `# Série Familie (extra) — Alles zusammen`
- Kit de Survie : `(1/3)`, `(2/3)`, `(3/3)`, puis `(extra)`

---

## Structure d'une fiche

### Fiches d'introduction (00_Introduction_*)

- Où parle-t-on allemand, une langue déjà familière, prononciation, nombres
- Pas d'explications longues

### Fiches d'apprentissage (01 à 04)

```markdown
# Série NOM (X/5) — Titre en allemand

@ img/theme.jpg | Légende de l'image avec source

Courte intro sympathique (1-2 phrases, pas un paragraphe).

---

## Les nouveaux mots

| Deutsch | Français |
|---------|----------|
| die Schule | l'école |
| ... | ... |

(6-7 mots essentiels ; un mot déjà vu est marqué « (rappel) »)

---

## Aujourd'hui on apprend...

### Un point de grammaire

Explication courte en français, rattachée aux mots ci-dessus.
Tableau d'exemples si utile.

---

## Des phrases

(6-7 cartes audio, progressives)

---

## On révise

(2 cartes qui réutilisent le vocabulaire des fiches/séries précédentes)

---

## 🇩🇪 Coin allemand

2 courts paragraphes sur la culture liés au thème.
Utiliser {{prononçable}} pour les mots-clés.

---

## Vocabulaire complémentaire

(2-3 mots, pas plus)

---

## Encore quelques phrases

(3 cartes audio avec le vocabulaire complémentaire)
```

### Fiche 05 : Dialogue

```markdown
## Les personnages

- 🦊 Toi
- 🐰 Lea

---

## Le dialogue

! 🐰 Hallo! Wie geht's?
> Salut ! Ça va ?
> Hallo = salut
> Wie geht's = ça va
```

- 10-15 répliques formant une scène continue
- Réutilise le vocabulaire des fiches 01-04 (et des séries précédentes)
- 2-3 mots nouveaux maximum, **toujours signalés** : `+ Mot nouveau signalé : {{…}} = …`
- Suivie d'un Coin allemand et de 3 cartes « Encore quelques phrases »

### Fiche 06 : Extra

- Tableau de **tout** le vocabulaire de la série (y compris les mots signalés du dialogue)
- 15-18 cartes audio recombinant librement ce vocabulaire
- Sert de matière première pour les exercices
- Aucun mot nouveau (ou alors signalé par une remarque `+`)

---

## Les cartes audio en pratique

### Structure de base

```
! Wie heißt du?
> Comment tu t'appelles ?
> Wie heißt du = comment tu t'appelles
+ « du » = tu (informel)
```

- Première ligne `>` : la traduction naturelle.
- Lignes `>` suivantes : **la décomposition morceau par morceau**. Ne pas se contenter de répéter la phrase entière (`> Die Katze läuft schnell = le chat court vite`) : découper (`> Die Katze läuft = le chat court` / `> schnell = vite`). C'est ce qui aide l'enfant à réutiliser les morceaux.
- Lignes `+` : remarques, mot nouveau signalé, petite astuce.

### Dialogues : le marqueur de locuteur va APRÈS le « ! »

```
! 🦊 Hallo, ich bin [ASK_USER_NAME].
> Salut, je suis [ASK_USER_NAME].

! 🐰 Hallo! Wie geht's?
> Salut ! Ça va ?
```

⚠️ **Pas** `🐰 ! Hallo` : dans ce cas le convertisseur ne reconnaît pas la carte (paragraphe + citation, pas d'audio, pas de bouton « Lire le dialogue »).

---

## Illustrations

Chaque fiche a une illustration en tête :

```markdown
@ img/nom-du-theme.jpg | Légende : enfant faisant X, ou objet Y. Source : Wikimedia Commons
```

Tant que l'image n'est pas choisie : `@ TODO_img/choisir-image.jpg | TODO : choisir une image (…)`.

**Recommandations :**
- Adaptées aux enfants, diverses et joyeuses
- Issues de Wikimedia Commons (licence libre) ou réalisées spécifiquement
- ~600-800px de large, claires et engageantes
- Légende avec mention de la source et de la licence

---

## Coin allemand

À garder léger et amusant, et **vérifiable** (pas de chiffre ou de record approximatif) :

✅ **« Le sais-tu ? En allemand, il existe un mot pour... »**
✅ **« En allemand, on dit... quand on veut dire... »**
✅ Des choses qu'un enfant peut voir ou vivre : la Schultüte, l'Ampelmännchen, le Streichelzoo, Mensch ärgere dich nicht…

❌ À éviter : présupposer des connaissances de grammaire avancées
❌ À éviter : un ton trop formel ou scolaire, des clichés (« les Allemands adorent l'ordre »)

---

## Qualité de langue

- **Français** : naturel pour un enfant (~8-12 ans), pas trop formel. Attention aux tournures fautives (« très délicieux » → « vraiment délicieux » / « trop bon »).
- **Deutsch** : allemand courant, celui qu'un enfant allemand dirait.
- Éviter les idiomes qui ne se traduisent pas directement ; préférer une explication.

### Pièges déjà rencontrés (à ne pas refaire)

| ❌ | ✅ |
|----|----|
| Danke viel! | Vielen Dank! / Danke schön! |
| Schön, dich zu kennen | Schön, dich kennenzulernen / Freut mich |
| Ich bin verloren (= je suis fichu) | Ich habe mich verlaufen |
| Oma kocht einen Kuchen | Oma backt einen Kuchen |
| Die Ziege isst Gras | Die Ziege frisst Gras (animal → fressen) |
| Ich mag Pferde sehr | Ich mag Pferde sehr gern / Ich liebe Pferde |
| Danke für deine Hilfe (à un adulte inconnu) | Vielen Dank für Ihre Hilfe |
| Geh links! | Geh nach links! |

---

## Suivi et génération automatique

Tous les fichiers de contenu suivent le schéma de nommage pour que le système de build puisse automatiquement :
- Détecter la catégorie et l'ordre
- Générer la navigation
- Rattacher les exercices au matériel d'apprentissage
- Construire la table des matières

Pour vérifier une fiche avant de pousser, on peut builder localement avec le repo Slovingo :

```
python3 src/build.py --lang-dir ../slovingo-de-fr --static-dir static
```

Le nombre de cartes audio dans `json/*.content.json` doit correspondre au nombre de lignes `!` dans les `.md` (un écart signale une carte mal formée).

---

## Check-list rapide avant de publier une fiche

- [ ] Illustration choisie (ou TODO explicite)
- [ ] 6-7 nouveaux mots + 2-3 complémentaires maximum
- [ ] Cartes décomposées morceau par morceau (pas juste la phrase entière répétée)
- [ ] Explications de grammaire : quelques phrases, avec un tableau d'exemples
- [ ] Aucun mot inconnu non signalé dans les cartes
- [ ] Dialogue : syntaxe `! 🐰 …`, mots nouveaux signalés
- [ ] Coin allemand : 2 paragraphes, faits vérifiables
- [ ] Fiche extra (06) : tableau complet, aucun mot nouveau
- [ ] Noms de fichiers et titres selon le schéma, sous-groupe déclaré dans `lang.json`
- [ ] Ton encourageant, pas intimidant

---

## Prochaines étapes

1. Choisir les illustrations (toutes les fiches sont en TODO)
2. Tester avec un enfant, ajuster ton, rythme et quantité de vocabulaire
3. Vérifier/ajuster les exercices générés
4. Série 07+ : fêtes et moments de l'année, école, couleurs, corps, vêtements, météo
5. Explorer les adaptations de code (gamification, UI) si le besoin s'en fait sentir
