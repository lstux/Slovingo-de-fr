# Images thématiques pour Slovingo-de-fr

Ce dossier contient les images visuelles associées à chaque thème du cours.

## Structure

```
img/
├── style_introduction.jpg   # Kit de Survie - apprentissage initial
├── style_familie.jpg        # Familie - famille, relations
├── style_haus.jpg          # Haus - maison, intérieur
├── style_essen.jpg         # Essen - nourriture, repas
├── style_stadt.jpg         # Stadt - ville, lieux publics
├── style_tiere.jpg         # Tiere - animaux
├── style_spiele.jpg        # Spiele - jeux, loisirs
└── credits.txt             # Crédits et URLs sources
```

## Directives pour les images

✅ **Format** : JPEG
✅ **Taille** : ~600-800px de large
✅ **Résolution** : 72-150 dpi (web)
✅ **Source** : Wikimedia Commons (licence libre : CC0, CC-BY, Public Domain)
✅ **Contenu** : Adapté aux enfants (8-12 ans), joyeux, inclusif, coloré

## Obtenir les images

1. **Consulter** `docs/Images_recommandees.md` pour les URLs de chaque thème
2. **Télécharger** depuis Wikimedia Commons (ou trouver des alternatives)
3. **Placer** dans ce dossier avec le nom `style_<theme>.jpg`
4. **Mettre à jour** `credits.txt` avec l'URL source finale et la licence exacte

### Exemple avec wget

```bash
cd slovingo-de-fr/img

# Télécharger une image (remplacer l'URL par la vraie URL directe)
wget https://upload.wikimedia.org/wikipedia/commons/... -O style_introduction.jpg

# Vérifier
ls -lh style_introduction.jpg
```

## Notes

- Les fichiers `style_*.jpg` actuels sont des placeholders (vides)
- À chaque fois qu'une image est ajoutée, mettre à jour **`credits.txt`** avec :
  - `nom_du_fichier.jpg | URL_source_wikimedia | Licence_exacte`
- Les images doivent être libres de droits pour pouvoir être distribuées avec le cours
- Garder les noms de fichiers cohérents : `style_` + minuscules du subgroup

## Thèmes et idées visuelles

| Thème | Subgroup | Ambiance |
|-------|----------|----------|
| Intro | introduction | Enfants en classe, souriant, prêt à apprendre |
| Familie | familie | Parents et enfants ensemble, joyeux, inclusif |
| Haus | haus | Pièces de maison chaleureuses (salon, cuisine, chambre) |
| Essen | essen | Nourriture colorée, repas en famille, cuisine ludique |
| Stadt | stadt | Rue vivante, bâtiments, transport (bus, voiture) |
| Tiere | tiere | Animaux mignons et variés (chat, chien, oiseau, etc.) |
| Spiele | spiele | Enfants jouant, jeux de société, activités de groupe |

---

**Voir aussi** : `docs/Images_recommandees.md` pour des URLs de départ et `docs/Format-de-fr.md` pour l'usage des images dans les fiches.
