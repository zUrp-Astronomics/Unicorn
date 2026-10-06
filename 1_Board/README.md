# 1_Board

**Date** : 2026-10-06
**Statut** : gabarit — à adapter au projet
**Référencé par** : `README.md` (§ Arborescence)

Les fichiers de fabrication de la carte électronique, tels que les sort l'outil de CAO.

## Nommage

Les fichiers gardent les noms du projet mère, TeenAstro : le préfixe `TeenAstro_Redux`, puis la
carte, la version, l'indice `n` et la nature du fichier. Les séparateurs varient d'une carte à
l'autre : `TeenAstro_Redux__Main_Board_v2.6.4__1_schematics.pdf`,
`TeenAstro_Redux__SHC_v1.5.2__1_Schematics.pdf`, `TeenAstro_Redux_Brake_Module_v1.1_1_schematics.pdf`.

L'indice `n` dit la nature du fichier :

| n | fichier | exemple |
|---|---|---|
| 0 | la fiche de la carte (texte) | aucune carte n'a encore la sienne |
| 1 | le schéma, en PDF et en PNG | `TeenAstro_Redux__Main_Board_v2.6.4__1_schematics.pdf`, `…__1_schematics_logic.png`, `TeenAstro_Redux__SHC_v1.5.2__1_Schematics.png` |
| 2 | les vues : 3D (PNG + STEP), dessus, dessous | `TeenAstro_Redux__Main_Board_v2.6.4__2_3D-view.step`, `…__2_3D-view_top.png`, `…__2_2D-view_bot.png`, `TeenAstro_Redux__SHC_v1.5.2__2_3D.step` |
| 3 | les Gerber (RS-274X + perçages Excellon), zippés | `TeenAstro_Redux__Main_Board_v2.6.4__3_gerber.zip`, `TeenAstro_Redux__SHC_v1.5.2__3_Gerber.zip` |
| 4 | la nomenclature (références LCSC) | `TeenAstro_Redux__Main_Board_v2.6.4__4_BOM.xlsx` |
| 5 | le placement (coordonnées en mm) | `TeenAstro_Redux__Main_Board_v2.6.4__5_PnP.xlsx` |

L'indice 0, la fiche `_0-README.txt`, n'existe encore pour aucune carte. Elle suivra le modèle
`PRODUIT-vX.Y_0-README.txt` de ce dossier.

## Plusieurs cartes (arbitrage de l'humain)

Un **sous-dossier par carte, dans `1_Board/`** : `Main-board/` (la carte principale), `SHC/` (la
raquette) et `Brake-module/` (le module de frein). Chacun garde ses fichiers sous leurs noms
d'origine, qui portent déjà le nom de la carte. La fiche de chaque carte est à venir, modèle
`PRODUIT-vX.Y_0-README.txt` dans ce dossier.
