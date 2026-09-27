# Format Slovingo-de-fr

## Vue d'ensemble

Ce document décrit comment le contenu est structuré dans Slovingo-de-fr, en particulier les adaptations faites pour des enfants par rapport au format destiné aux adultes utilisé dans les autres cours Slovingo.

La base reste le **SMD (Slovingo Markdown)** — voir la [documentation Slovingo](https://github.com/lstux/Slovingo/tree/main/docs) (`Format-SMD.txt`) pour la référence technique complète.

## Adaptations pour les enfants

### 1. Un ton plus léger, plus ludique

**Cours adulte (sk-fr, fr-sk) :**
> Doslova „dobrý deň". Môžeš ho použiť v každej situácii, kde nepoznáš osobu.
> (Littéralement « bonne journée ». Tu peux l'utiliser dans toute situation où tu ne connais pas la personne.)

**Cours enfant (de-fr) :**
- Phrases plus courtes
- Plus de points d'exclamation et d'emojis
- Explications rattachées à des situations concrètes du quotidien d'un enfant
- Ton parfois familier, comme si on parlait à un copain

### 2. Des éléments visuels et interactifs

- **Plus d'illustrations** : chaque fiche a une image vivante et engageante (enfants, animaux, activités)
- **Marqueurs emoji** : usage plus généreux pour les personnages, les émotions, les thèmes
- **Exercices variés** : pas seulement « écoute et traduis » — appariement, vrai/faux, mise en situation
- **Prêt pour la gamification** : la structure permet d'ajouter étoiles, badges, séries de jours consécutifs

### 3. Une progression de série adaptée

On garde la structure **intro/séries/vocabulaire/annexes** des cours adultes, mais chaque série vise :

- **4 fiches** (au lieu de 5) : vocabulaire essentiel uniquement, leçons plus courtes
- **1 fiche dialogue** : conversation ludique (pas une mini-histoire complète)
- **1 fiche extra** : récapitulatif du vocabulaire + base pour les exercices

Cela rend l'apprentissage plus digeste pour des enfants avec une attention plus courte.

### 4. Des dialogues portés par des personnages — et par l'enfant lui-même

Les enfants s'investissent mieux avec des personnages récurrents :
- Un adulte bienveillant (parent, professeur, grand-parent)
- Éventuellement un animal 🐶

Les dialogues remobilisent le vocabulaire de la série dans des contextes amusants : demander de l'aide, se perdre, commander à manger, etc.

**Le protagoniste, c'est l'enfant lui-même.** Slovingo fournit un mécanisme intégré pour ça (déjà utilisé dans le cours sk-fr) :

- **`[ASK_USER_NAME]`** : insère un champ de saisie directement dans le texte, la première fois qu'on demande le prénom (ex. `Ich heiße [ASK_USER_NAME].`)
- **`[USER_NAME]`** : réutilise ensuite ce prénom partout où on veut personnaliser (ex. `Schön, dich zu kennen, [USER_NAME]!`)
- **Emoji du locuteur : `🦊`** — une tête d'animal pour le personnage-utilisateur plutôt qu'une silhouette humaine, plus ludique et qui évite d'avoir à choisir un genre. Tous les personnages récurrents suivent ce principe (têtes d'animaux) : voir la liste des personnages dans [Progression.md](./Progression.md).

Le nom de secours (si l'enfant n'a rien saisi) vient de `lang.json` → `site.user_name_default`, et le texte du champ de `site.user_name_placeholder`.

À utiliser dès qu'un dialogue met en scène l'enfant qui apprend : ça personnalise l'expérience sans dupliquer le contenu ni se soucier du genre du personnage.

---

## Structure des fichiers

```
slovingo-de-fr/md/
├── 00_Introduction_*.md          # Fiches d'intro (comment utiliser, alphabet, sons...)
├── 10_Series_XX_Theme_YY_*.md    # Séries d'apprentissage
├── 20_Vocabulary_*.md            # Listes de vocabulaire autonomes (par thème ou niveau)
└── 30_Annex_*.md                 # Notes culturelles, tableaux de grammaire, etc.
```

### Numérotation des séries

- **Série 00** : Kit de Survie (phrases de base)
- **Série 01+** : progressions thématiques (Familie, Haus, Essen, etc.)

Exemple de nom de fichier : `10_Series_01_Familie_02_das-zuhause.md`

---

## Structure d'une fiche

### Fiches d'introduction (00_Introduction_*)

- Intro rapide et sympathique au cours
- Alphabet + prononciation (sons allemands pour francophones)
- Compter (0-10, puis 10-100)
- Pas d'explications longues — renvoyer vers la doc Slovingo principale si besoin de détails

### Fiches de série (10_Series_XX_*)

**Fiches 01 à 04 : fiches d'apprentissage**

```markdown
# Série NOM (X/Y) — Titre en allemand

@ img/theme.jpg | Légende de l'image avec source

Courte intro sympathique (1-2 phrases, pas un paragraphe).

---

## Die neuen Wörter (Les nouveaux mots)

| Deutsch | Français |
|---------|----------|
| Hallo | Bonjour |
| ... | ... |

(~7 mots essentiels)

---

## Heute lernen wir... (Aujourd'hui on apprend...)

### Un point de grammaire

Explication courte en français, rattachée aux mots ci-dessus.

| Deutsch | Français |
|---------|----------|
| Ich heiße Anna. | Je m'appelle Anna. |
| ... | ... |

---

## Sätze (Des phrases)

! Hallo!
> Bonjour !
> Hallo = bonjour
+ Salutation informelle, entre amis ou en famille.

(6-8 cartes audio, progressives)

---

## Das wiederholen wir (On révise)

(À partir de la série 02 : réutilise exclusivement le vocabulaire des fiches précédentes)

---

## 🇩🇪 Coin allemand

2-3 courts paragraphes sur la culture allemande liés au thème.
Utiliser {{prononçable}} pour les mots-clés.

---

## Mehr Wörter (Vocabulaire complémentaire)

| Deutsch | Français |
|---------|----------|
| ... | ... |

(~7 mots supplémentaires/complémentaires)

---

## Noch mehr Sätze (Encore quelques phrases)

(3-5 cartes audio avec le vocabulaire complémentaire)
```

**Fiche 05 : Dialogue**

- Mini-histoire ou dialogue suivi avec les personnages récurrents
- Réutilise tout le vocabulaire des fiches 01-04
- Aucun mot nouveau (ou signalé explicitement si indispensable)
- 8-12 cartes audio formant un échange continu

**Fiche 06 : Extra**

- Tableau de vocabulaire complet de la série
- 15-20 cartes audio recombinant librement le vocabulaire
- Sert de matière première pour les exercices
- Aucun apprentissage nouveau — uniquement révision et réemploi

---

## Les cartes audio en pratique

### Structure de base

```
! Wie heißt du?
> Comment t'appelles-tu ?
> Wie heißt du = comment t'appelles-tu
+ « du » = tu (informel)
```

### Avec marqueurs de locuteur (dialogues)

```
👦 ! Hallo, ich bin Tom.
> Salut, je m'appelle Tom.

👩 ! Hallo Tom! Wie geht's?
> Salut Tom ! Ça va ?
```

### Avec notes culturelles

```
! Guten Morgen!
> Bonjour ! (littéralement : bon matin)
+ Très formel. Utilisé avec les professeurs, les inconnus, etc.
```

---

## Illustrations

Chaque fiche a une illustration en tête :

```markdown
@ img/nom-du-theme.jpg | Légende : enfant faisant X, ou objet Y. Source : Wikimedia Commons
```

**Recommandations :**
- Adaptées aux enfants, diverses et joyeuses
- Issues de Wikimedia Commons (licence libre) ou réalisées spécifiquement
- ~600-800px de large, claires et engageantes
- Légende avec mention de la source et de la licence

---

## Notes de langue (Coin allemand)

À garder léger et amusant :

✅ **« Le sais-tu ? En allemand, il existe un mot pour... »**
✅ **« En allemand, on dit... quand on veut dire... »**
✅ **« Anecdote : [détail culturel] est très important en Allemagne »**

❌ À éviter : présupposer des connaissances de grammaire avancées
❌ À éviter : un ton trop formel ou scolaire

---

## Listes de vocabulaire (20_Vocabulary_*)

Documents de référence autonomes :

- Organisés par thème (Farben = couleurs, Tiere = animaux)
- Ou par niveau (A1, A2, A3)
- Tableaux simples : Deutsch | Français | Prononciation
- Pas de cartes audio

---

## Annexes (30_Annex_*)

Tableaux de grammaire, conjugaison, règles de genre, etc. :

- Matériel de référence (pas destiné à l'apprentissage direct)
- Peut être plus aride/académique puisqu'il est en support, pas en contenu principal
- Lié depuis les fiches de série quand c'est pertinent

---

## Qualité de traduction

- Français : naturel pour un enfant (~8-12 ans), pas trop formel
- Deutsch : allemand courant et pratique pour apprenants
- Éviter les idiomes qui ne se traduisent pas directement ; préférer une explication

---

## Suivi et génération automatique

Tous les fichiers de contenu suivent le schéma de nommage pour que le système de build puisse automatiquement :
- Détecter la catégorie et l'ordre
- Générer la navigation
- Rattacher les exercices au matériel d'apprentissage
- Construire la table des matières

Voir [../lang.json](../lang.json) et la documentation Slovingo principale pour les détails d'implémentation.

---

## Check-list rapide avant de publier une fiche

- [ ] Illustration claire, adaptée aux enfants, diverse
- [ ] Vocabulaire cumulatif (réutilise les fiches précédentes)
- [ ] Explications de grammaire : 1-2 phrases maximum
- [ ] Cartes audio jouables (pas de vocabulaire inconnu)
- [ ] Dialogue des personnages naturel (pas scolaire)
- [ ] Coin allemand : ~3 courts paragraphes (culture, pas grammaire)
- [ ] Fiche extra (06) : aucun mot nouveau
- [ ] Tous les noms de fichiers suivent le schéma
- [ ] Ton encourageant, pas intimidant

---

## Prochaines étapes

1. Construire la première série (Kit de Survie)
2. Recueillir les retours des tests avec un enfant
3. Ajuster le ton, le rythme, les illustrations
4. Ajouter les exercices une fois les séries 0-1 stabilisées
5. Explorer les adaptations de code (gamification, UI) si le besoin s'en fait sentir
