# 9_Assets

**Date** : 2026-10-06
**Statut** : gabarit — à adapter au projet
**Référencé par** : `README.md` (§ Arborescence), le site zurp-astronomics.github.io

Les ressources du projet pour l'extérieur : images des README et de la doc, et la **vitrine** lue
par le site de l'org.

| fichier | rôle |
|---|---|
| `zurp.yml` | la fiche vitrine, lue par le site au build |
| `<slug>.png` | l'affiche, nommée par le champ `poster:` de la fiche, 1254 × 1254 |
| le reste | les PNG des README et de la doc, librement |

Le site ne lit **que** ce dossier, plus ce que GitHub sait du dépôt (releases, licence détectée dans
`LICENSE`). Tout push dans `9_Assets/` sur `main` reconstruit le site
(`.github/workflows/zurp-site.yml`).
