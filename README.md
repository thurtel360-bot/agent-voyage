# Agent de voyage — veille all inclusive

Site statique qui affiche les résultats de la veille automatique (séjours all inclusive en famille, Avril & Août 2027, budget 2 500 €).

- `index.html` : la page (aucune dépendance, lit les fichiers de `data/`).
- `data/latest.json` : résultat de la dernière veille.
- `data/runs/AAAA-MM-JJ.json` + `data/runs/index.json` : archive des veilles (sélecteur « Veille du »).
- `data/historique_avril.csv`, `data/historique_aout.csv` : historique des prix (graphique d'évolution).

## Publication
Activer GitHub Pages : *Settings → Pages → Deploy from a branch → `main` / root*.
Le site sera alors visible sur https://thurtel360-bot.github.io/agent-voyage/

## Mise à jour
À chaque veille, la tâche planifiée réécrit `data/latest.json`, ajoute `data/runs/<date>.json`, met à jour `data/runs/index.json` et les deux CSV, puis pousse sur `main`.
