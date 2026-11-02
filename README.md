# Carte Cohorte 2026 — XD Textile Responsable

Carte des **38 projets territoriaux** de la cohorte 2026 de l'Extrême Défi Textile Responsable (ADEME), conçue par [TINYLABS](https://tinylabs.one).

*Map of the 38 territorial projects in the 2026 cohort of ADEME's Extrême Défi Textile Responsable.*

**→ [Voir la carte](https://justynaswat-dotcom.github.io/carte-cohorte/)**

## Ce que montre la carte

- Un point par projet, à son adresse (registre SIRENE) ou, à défaut, au centre de la commune
- Le nombre de projets par région
- Les Outre-mer en encarts, seulement ceux qui ont des projets
- Un clic sur une région ouvre la page de ses projets sur le site de l'ADEME

La carte est volontairement fixe (ni zoom ni déplacement) et pensée pour être intégrée en iframe. Elle remplit le cadre qui l'accueille et passe en mode compact sous 640 px de large (téléphones).

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | La carte : HTML, CSS et JS dans un seul fichier |
| `data/projets.json` | Projets (région, coordonnées, précision), liens vers les pages régionales, placement des étiquettes |
| `data/regions.geojson` | Contours des régions |
| `data/france.geojson` | Contour du territoire, qui sert de masque au relief |

## Intégration

```html
<iframe src="https://justynaswat-dotcom.github.io/carte-cohorte/"
        style="width:100%; aspect-ratio:16/9; border:0"
        title="Carte des projets de la cohorte 2026"></iframe>
```

## Mettre à jour les projets

Modifier `data/projets.json`, puis pousser sur `main` : GitHub Pages republie la carte automatiquement.

## Sources et outils

- Fond de carte : [Leaflet](https://leafletjs.com) 1.9.4
- Relief (estompage) : IGN, Géoplateforme
- Contours administratifs : Etalab
- Typographie : DM Sans
