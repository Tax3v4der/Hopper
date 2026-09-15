# Hopper — État des hoppers, Atelier A Injection

Relevé de l'état des trémies (hoppers) des presses à injection de l'atelier A,
Thermoplastic Tunisia. Page statique, mobile first, sans dépendance.

## Contenu

- `index.html` — page unique (HTML + CSS + JS en ligne), ouvrable directement dans un navigateur
- `img/` — 31 photos, une par machine, repère machine incrusté en haut à droite

## Relevé du 15/09/2026 — 31 machines

| État | Nb | Machines |
|---|---|---|
| Résistances et moteur OK | 12 | Mc1, Mc11, Mc12, Mc21, Mc22, Mc26, Mc27, Mc29, Mc30, Mc32, Mc35, 200 |
| Moteur manquant | 6 | Mc4, Mc7, Mc8, Mc10, Mc28, Mc33 |
| Résistance HS | 1 | Mc25 |
| Trémie sans déshumidificateur | 6 | Mc2, Mc3, Mc6, Mc15, Mc34, Mc36 |
| Trémie simple | 6 | Mc5, Mc9, Mc13, Mc14, Mc16, Mc31 |

Mc23 et Mc24 sont hors service et ne figurent pas au relevé.
Les trémies mobiles ne sont pas incluses.

## À vérifier

- Les 6 machines classées « sans déshumidificateur » sont déduites par élimination,
  pas relevées une par une. Mc1 était dans ce lot et s'est révélé conforme.
- Les résistances des 6 machines sans moteur n'ont pas pu être essayées.

## Mettre à jour un état

Modifier le tableau `DATA` dans `index.html` : le champ `status` accepte
`ok`, `heater`, `motor`, `nodryer`, `simple`. Le champ `note` s'affiche sous l'état
quand il n'est pas vide. Les compteurs et les filtres se recalculent tout seuls.
