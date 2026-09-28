# Images des thèmes (`img/style_*.jpg`)

Candidats pour les photos de fond des thèmes CSS. Chaque titre ci-dessous est apparu dans une recherche sur Wikimedia Commons, donc le fichier existe. En revanche, **la licence, l'auteur et le rendu réel n'ont pas été vérifiés** (les pages de fichiers n'étaient pas consultables) : à contrôler sur la page avant de garder une image, puis à reporter dans `img/credits.txt`.

## Ce qu'on cherche

Dans `static/style.css` (repo Slovingo), ces images sont des fonds de bandeau (`--band-height: 220px`) passés en niveaux de gris et teintés (`--photo-grayscale`, `--photo-tint`). Il faut donc :

- une photo **large, en paysage**, avec un sujet lisible même en 220 px de haut ;
- peu de détails fins et de texte ;
- inutile qu'elle soit « mignonne » : la teinte du thème fait le gros du travail.

Note : le CSS du repo Slovingo déclare aujourd'hui `--photo-uvod`, `--photo-rodina`, etc. (thèmes slovaques). Il faudra prévoir les variables `--photo-familie`, `--photo-haus`… côté Slovingo.

On ne réutilise pas les images du cours slovaque : chaque thème de-fr a sa propre photo.

## Choix retenus

Images à télécharger puis à placer dans `img/` (licences à vérifier sur chaque page, puis à compléter dans `credits.txt`) :

| Fichier | Image choisie |
|---------|---------------|
| `style_introduction.jpg` | https://commons.wikimedia.org/wiki/File:Hohenpei%C3%9Fenberg_Panorama.jpg |
| `style_kitsurvie.jpg` | https://commons.wikimedia.org/wiki/File:Beetzendorf_Willkommen.jpg |
| `style_familie.jpg` | à choisir (piste : famille en contre-jour au coucher du soleil, voir plus bas) |
| `style_haus.jpg` | https://commons.wikimedia.org/wiki/File:Nordisches_Einfamilienhaus.jpg |
| `style_essen.jpg` | https://commons.wikimedia.org/wiki/File:Brotscheiben_auf_dem_Fr%C3%BChst%C3%BCckstisch.jpg |
| `style_stadt.jpg` | https://commons.wikimedia.org/wiki/File:Fu%C3%9Fg%C3%A4ngerzone_Rastatt.JPG |
| `style_tiere.jpg` | https://commons.wikimedia.org/wiki/File:Kuehe_Weide_Cows_Pasture.jpg |
| `style_spiele.jpg` | https://commons.wikimedia.org/wiki/File:Children_Playing_in_Playground.jpg |

## Candidats par thème

### Introduction (équivalent de `uvod`)
- https://commons.wikimedia.org/wiki/Category:Schult%C3%BCte (la cône de rentrée, très « allemand »)
- https://commons.wikimedia.org/wiki/Category:School_children_of_Germany
- https://commons.wikimedia.org/wiki/File:Hohenpei%C3%9Fenberg_Panorama.jpg (paysage bavarois, panorama)
- https://commons.wikimedia.org/wiki/File:Hohenschwangau_village_%28Bavaria%29_%283%29.jpg
- https://commons.wikimedia.org/wiki/File:Buching_Halblech_Alpine_Village.jpg

### Kit de Survie (image à part)
Thème : salutations, politesse, premiers mots. Pas de bonne photo d'enfants qui se saluent trouvée ; la piste la plus parlante est le panneau d'accueil multilingue (« Willkommen » et « Bienvenue » côte à côte) :
- https://commons.wikimedia.org/wiki/File:Welkom_willkommen_Welcome_Bienvenue_Benvenuto.jpg
- https://commons.wikimedia.org/wiki/File:Welkom_willkommen_Welcome_Bienvenue_Benvenuto_%28cropped%29.jpg (version recadrée)
- https://commons.wikimedia.org/wiki/Category:Welcome_signs_in_Germany
- https://commons.wikimedia.org/wiki/Category:Welcome_signs
- https://commons.wikimedia.org/wiki/Category:Hello
- https://commons.wikimedia.org/wiki/Category:Welcoming
- https://commons.wikimedia.org/wiki/Category:Hand_waving
- https://commons.wikimedia.org/wiki/File:Handshake.jpg (poignée de main, sujet adulte)
- https://commons.wikimedia.org/wiki/File:Multilingual_speech_bubble.svg (SVG, pas une photo)

### Familie
- https://commons.wikimedia.org/wiki/File:Family_eating_meal.jpg
- https://commons.wikimedia.org/wiki/File:A_family_and_guests_at_the_table_sharing_a_meal.jpg
- https://commons.wikimedia.org/wiki/Category:Families_eating

### Haus
- https://commons.wikimedia.org/wiki/Category:Houses_in_Germany
- https://commons.wikimedia.org/wiki/File:Half-timbered-house_lerbach-osterode-germany.png
- https://commons.wikimedia.org/wiki/Category:Children%27s_rooms

### Essen
- https://commons.wikimedia.org/wiki/File:Brotscheiben_auf_dem_Fr%C3%BChst%C3%BCckstisch.jpg
- https://commons.wikimedia.org/wiki/File:Breakfast_table.JPG
- https://commons.wikimedia.org/wiki/File:Bread_rolls.JPG
- https://commons.wikimedia.org/wiki/Category:Breads_of_Germany
- https://commons.wikimedia.org/wiki/Category:Pretzels

### Stadt
- https://commons.wikimedia.org/wiki/File:Fu%C3%9Fg%C3%A4ngerzone_Rastatt.JPG (zone piétonne)
- https://commons.wikimedia.org/wiki/File:Rostock_Innenstadt.JPG
- https://commons.wikimedia.org/wiki/File:Bergheim_Innenstadt.JPG
- https://commons.wikimedia.org/wiki/File:D%C3%BClmen%2C_Marktplatz_--_2012.jpg
- https://commons.wikimedia.org/wiki/File:Alter_Markt_%28Old_Market%29_in_Magdeburg%2C_Germany_%2835906583011%29.jpg
- https://commons.wikimedia.org/wiki/File:Traffic_Light_German_Complex_With_Bicycles.JPG (feu allemand avec vélos)
- https://commons.wikimedia.org/wiki/File:Ampelm%C3%A4nnchen_in_Berlin.JPG (l'Ampelmännchen est cité dans le Coin allemand de la doc de format)
- https://commons.wikimedia.org/wiki/File:DDR_Ampelm%C3%A4nnchen_-_rot.JPG
- https://commons.wikimedia.org/wiki/Category:Tram_tracks_in_Germany
- https://commons.wikimedia.org/wiki/Category:Streets_in_Germany_by_city

### Tiere
- https://commons.wikimedia.org/wiki/File:Kuehe_Weide_Cows_Pasture.jpg (vaches au pré, nom allemand)
- https://commons.wikimedia.org/wiki/File:Holstein_Cow_Grazing_01.jpg (existent aussi : `_02` et `_04`)
- https://commons.wikimedia.org/wiki/File:Goat_at_petting_zoo.png (Streichelzoo, mais lieu non allemand)
- https://commons.wikimedia.org/wiki/File:Chinguacousy_Park_Petting_Zoo_2022.jpg (idem)

### Spiele
- https://commons.wikimedia.org/wiki/File:Family_playing_a_board_game_%283%29.jpg
- https://commons.wikimedia.org/wiki/File:Playing_board_game_-_Play_578_1699743964830.jpg
- https://commons.wikimedia.org/wiki/File:Kids_playing_carrom_board.jpeg
- https://commons.wikimedia.org/wiki/File:Playground.jpg (aire de jeux)
- https://commons.wikimedia.org/wiki/File:Children_Playing_in_Playground.jpg
- https://commons.wikimedia.org/wiki/Category:Children%27s_board_games
- https://commons.wikimedia.org/wiki/Category:Children%27s_games

## À vérifier en vrai

- **Kit de Survie** : le panneau multilingue est un bon candidat, mais à voir (cadrage, lisibilité une fois teinté en 220 px).
- **Stadt** : plusieurs pistes, à choisir à l'œil.

## Procédure

1. Ouvrir la page du fichier, vérifier licence et auteur.
2. Télécharger l'original, recadrer en paysage, ~1200 px de large, JPEG.
3. Enregistrer sous `img/style_<nom>.jpg`.
4. Ajouter dans `img/credits.txt` : fichier, URL source, licence, auteur.
