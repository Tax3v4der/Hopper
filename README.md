# Hopper — État des hoppers, Atelier A Injection

Relevé de l'état des trémies (hoppers) des presses à injection de l'atelier A,
Thermoplastic Tunisia. Page statique, mobile first, sans dépendance.

## Contenu

- `index.html` — page unique (HTML + CSS + JS en ligne), ouvrable directement dans un navigateur
- `img/` — photos de trémie (Mob2 et Mob3 partagent `img/mob23.jpg`), une par machine, repère machine incrusté en haut à droite
- `cab/` — 23 photos d'armoire électrique, pour les trémies équipées d'un déshumidificateur
- `logo.svg`, `favicon.ico` — logo Bilel Adel : en-tête de page et icône d'onglet

## Relevé du 15/09/2026 — 39 trémies

| État | Nb | Machines |
|---|---|---|
| Résistances et moteur OK | 17 | Mc1, Mc11, Mc12, Mc21, Mc22, Mc26, Mc27, Mc29, Mc30, Mc32, Mc35, 200, Bat6, Mob1, Mob2, Mob3, Mob4 |
| Moteur manquant | 6 | Mc4, Mc7, Mc8, Mc10, Mc28, Mc33 |
| Résistance HS | 1 | Mc25 |
| Trémie sans déshumidificateur | 6 | Mc2, Mc3, Mc6, Mc15, Mc34, Mc36 |
| Trémie simple | 8 | Mc5, Mc9, Mc13, Mc14, Mc16, Mc31, Bat4, Bat5 |
| Neuve, en attente de mise en service | 1 | Mob5 |

Mc23 et Mc24 sont hors service et ne figurent pas au relevé.
Les trémies mobiles Mob1 à Mob5 sont incluses depuis le relevé du 15/09.
Les armoires électriques ne concernent que les 23 trémies équipées d'un
déshumidificateur : trémies simples et trémies sans déshumidificateur en sont exclues.

## À vérifier

- Les 6 machines classées « sans déshumidificateur » sont déduites par élimination,
  pas relevées une par une. Mc1 était dans ce lot et s'est révélé conforme.
- Les résistances des 6 machines sans moteur n'ont pas pu être essayées.

## Mettre à jour un état

Modifier le tableau `DATA` dans `index.html` : le champ `status` accepte
`ok`, `heater`, `motor`, `nodryer`, `simple`, `pending`, `unknown`.
Le champ `mob` à 1 place la trémie dans la section « Trémies mobiles ». Le champ `note` s'affiche sous l'état
quand il n'est pas vide. Une machine sans photo laisse `slug` vide et
affiche un cartouche « Photo à venir ». Le champ `cab` pointe vers
`cab/<valeur>.jpg` et ajoute la vignette d'armoire sous l'état. Les compteurs et les filtres se recalculent tout seuls.
