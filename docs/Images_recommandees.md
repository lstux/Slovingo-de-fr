# Images des thèmes (`img/style_*.jpg`)

Candidats pour les photos de fond des thèmes CSS. Chaque titre ci-dessous est apparu dans une recherche sur Wikimedia Commons, donc le fichier existe. En revanche, **la licence, l'auteur et le rendu réel n'ont pas été vérifiés** (les pages de fichiers n'étaient pas consultables) : à contrôler sur la page avant de garder une image, puis à reporter dans `img/credits.txt`.

## Ce qu'on cherche

Dans `static/style.css` (repo Slovingo), ces images sont des fonds de bandeau (`--band-height: 220px`) passés en niveaux de gris et teintés (`--photo-grayscale`, `--photo-tint`). Il faut donc :

- une photo **large, en paysage**, avec un sujet lisible même en 220 px de haut ;
- peu de détails fins et de texte ;
- inutile qu'elle soit « mignonne » : la teinte du thème fait le gros du travail.

Note : le CSS du repo Slovingo déclare aujourd'hui `--photo-uvod`, `--photo-rodina`, etc. (thèmes slovaques). Il faudra prévoir les variables `--photo-familie`, `--photo-haus`… côté Slovingo.

## Candidats par thème

Base : `https://commons.wikimedia.org/wiki/`

### Introduction (équivalent de `uvod`)
- `Category:Schultüte` (la cône de rentrée, très « allemand »)
- `Category:School_children_of_Germany`
- `File:Hohenpeißenberg_Panorama.jpg` (paysage bavarois, panorama)
- `File:Hohenschwangau_village_(Bavaria)_(3).jpg`
- `File:Buching_Halblech_Alpine_Village.jpg`

### Familie
- `File:Family_eating_meal.jpg`
- `File:A_family_and_guests_at_the_table_sharing_a_meal.jpg`
- `Category:Families_eating`

### Haus
- `Category:Houses_in_Germany`
- `File:Half-timbered-house_lerbach-osterode-germany.png`
- `Category:Children's_rooms`

### Essen
- `File:Brotscheiben_auf_dem_Frühstückstisch.jpg`
- `File:Breakfast_table.JPG`
- `File:Bread_rolls.JPG`
- `Category:Breads_of_Germany`, `Category:Pretzels`

### Stadt
- `File:Dülmen,_Marktplatz_--_2012.jpg`
- `File:Alter_Markt_(Old_Market)_in_Magdeburg,_Germany_(35906583011).jpg`

### Tiere
- `File:Kuehe_Weide_Cows_Pasture.jpg` (vaches au pré, nom allemand)
- `File:Holstein_Cow_Grazing_01.jpg` (et `_02`, `_04`)
- `File:Goat_at_petting_zoo.png`, `File:Chinguacousy_Park_Petting_Zoo_2022.jpg` (Streichelzoo, mais lieux non allemands)

### Spiele
- `File:Family_playing_a_board_game_(3).jpg`
- `File:Playing_board_game_-_Play_578_1699743964830.jpg`
- `File:Kids_playing_carrom_board.jpeg`
- `Category:Children's_board_games`, `Category:Children's_games`

## Encore à trouver

- **Stadt** : les deux candidats sont des places de marché ; une vue de rue plus vivante serait mieux.
- **Kit de Survie** : dans sk-fr il n'y a pas d'image dédiée (il partage `uvod`) ; à confirmer pour de-fr.

## Procédure

1. Ouvrir la page du fichier, vérifier licence et auteur.
2. Télécharger l'original, recadrer en paysage, ~1200 px de large, JPEG.
3. Enregistrer sous `img/style_<nom>.jpg`.
4. Ajouter dans `img/credits.txt` : fichier, URL source, licence, auteur.
