# Documentation de Slovingo-de-fr

Bienvenue ! Ce dossier contient les guides pour comprendre et contribuer au projet Slovingo-de-fr.

## 📖 Par où commencer ?

**Nouveau sur le projet ?**
- Lire d'abord [../README.md](../README.md) pour la vue d'ensemble
- Puis revenir ici pour le détail

**Envie d'écrire du contenu (fiches) ?**
- Commencer par **[Format-de-fr.md](./Format-de-fr.md)** — comment structurer une fiche et utiliser le format SMD
- Puis **[Progression.md](./Progression.md)** — comprendre le parcours d'apprentissage et ce qu'on enseigne à quel moment

**Envie de comprendre l'approche pédagogique ?**
- Voir **[Progression.md](./Progression.md)** — philosophie pédagogique et structure des séries

**Besoin de détails techniques ?**
- Se référer à la **[documentation Slovingo principale](https://github.com/lstux/Slovingo/tree/main/docs)** pour :
  - La référence complète du format SMD (`Format-SMD.txt`)
  - Le pipeline de build et la CI (`CI-Pipeline.md`)
  - Les conventions de nommage des fichiers (`Fiches-Serie.txt`)

## 📁 Fichiers de ce dossier

| Fichier | Rôle |
|---------|------|
| **Format-de-fr.md** | Comment écrire des fiches pour enfants — structure, ton, exemples |
| **Progression.md** | Feuille de route pédagogique — quoi enseigner, dans quel ordre, pourquoi |
| **README.md** | Vous êtes ici ! |

## 🚀 Workflow rapide

### Pour écrire une nouvelle fiche :

1. Décider de la série et du numéro de fiche (ex. Série 01, fiche 02)
2. Ouvrir **[Format-de-fr.md](./Format-de-fr.md)** pour voir le gabarit
3. Écrire la fiche dans `/md/` en respectant le schéma de nommage
4. Ajouter une illustration dans `/img/`
5. Parcourir la check-list en bas de [Format-de-fr.md](./Format-de-fr.md) (notamment la syntaxe des dialogues `! 🐰 …` et le tableau « Pièges déjà rencontrés »)
6. Commit et push sur le dépôt

### Pour ajouter des exercices :

1. Écrire d'abord la fiche (elle doit être stable : chaque exercice reprend mot pour mot une ligne de tableau ou une carte)
2. Écrire `exercises/<nom de la fiche>.exercises.json` en suivant les règles de la section « Exercices faits main » de [Format-de-fr.md](./Format-de-fr.md)
3. Builder localement : aucun avertissement d'exercice périmé ne doit apparaître

### Pour vérifier les textes d'interface :

Quand le moteur Slovingo gagne une fonction, il peut lui manquer des textes dans `lang.json` → `ui` (l'enfant verrait alors de l'anglais). Le build affiche un avertissement ; pour le détail, avec le texte anglais à traduire :

```
python3 src/check_ui_keys.py --lang-dir <chemin du cours> --template
```

(depuis une copie de [lstux/Slovingo](https://github.com/lstux/Slovingo) — voir [Lang-json.md](https://github.com/lstux/Slovingo/blob/main/docs/Lang-json.md)). Le cours est écrit en tutoiement et avec des mots simples (« Choisir », « Relier », « Bravo ! »), comme la fiche « Comment ça marche ».

### Pour itérer sur la pédagogie :

1. Tester les fiches avec des enfants
2. Documenter ce qui marche/ne marche pas
3. Ajuster ton, rythme, vocabulaire si besoin
4. Mettre à jour cette doc si l'approche change

## 🔗 Documentation liée

- **[Dépôt Slovingo principal](https://github.com/lstux/Slovingo)** → framework technique, code, système de build
- **[Format-SMD.txt](https://github.com/lstux/Slovingo/blob/main/docs/Format-SMD.txt)** → format SMD complet (celui qu'on utilise ici)
- **[Fiches-Serie.txt](https://github.com/lstux/Slovingo/blob/main/docs/Fiches-Serie.txt)** → structure de série adulte (qu'on adapte pour les enfants)

## 💡 Principes de conception

Les documents de format et de progression reposent sur ces idées centrales :

1. **Les enfants apprennent en jouant** — ton léger, structure claire
2. **La progression est visible** — une série se termine en ~1 semaine, une fiche en ~1 jour
3. **La répétition fonctionne** — le vocabulaire est réemployé, renforcé, approfondi
4. **La culture compte** — les enfants veulent savoir *pourquoi* ils apprennent l'allemand
5. **La flexibilité prime** — adapter format et code selon ce que les tests réels montrent

## ❓ Des questions ?

- **Sur l'approche pédagogique ?** → Voir [Progression.md](./Progression.md)
- **Sur le format et l'écriture des fiches ?** → Lire [Format-de-fr.md](./Format-de-fr.md)
- **Sur la syntaxe SMD ou le système de build ?** → Voir la [documentation Slovingo principale](https://github.com/lstux/Slovingo/tree/main/docs)

---

**Statut :** 🚀 La documentation évolue avec le contenu. À revoir au fur et à mesure qu'on ajoute des fiches et qu'on découvre ce qui fonctionne.
