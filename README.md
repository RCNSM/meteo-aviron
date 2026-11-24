# Météo aviron — RCNSM

Petite appli web (PWA) météo pour la section aviron du RCNSM (club nautique de
Wépion) : météo, vent, alertes et débit de la Meuse. Elle s'installe sur l'écran d'accueil du téléphone.

Adresse : https://meteo.rcnsm.be

## Fonctionnement

- Appli 100 % statique : pas de code serveur, pas de service worker, pas de clé d'API.
- Le téléphone interroge directement Open-Meteo (`api.open-meteo.com`), l'IRM
  (`app.meteo.be`) et l'hydrométrie du SPW (`hydrometrie.wallonie.be`).
- Hébergement : GitHub Pages, branche `main`, dossier racine. Le fichier `.nojekyll`
  désactive le traitement Jekyll ; le fichier `CNAME` porte le domaine personnalisé.

## Mettre à jour l'appli

1. Remplacer les fichiers modifiés dans ce dossier (garder `polices/`, `.nojekyll` et `CNAME`).
2. Publier :

   ```bash
   git add -A
   git commit -m "Description de la modification"
   git push
   ```

3. GitHub Pages republie le site en une à deux minutes. Sur le téléphone, recharger
   la page (ou fermer puis rouvrir l'appli installée).

## Domaine

Le sous-domaine `meteo.rcnsm.be` pointe vers GitHub Pages par une ligne CNAME dans la
zone DNS de rcnsm.be (gérée par l'administrateur web du club). Si ce dépôt est un jour
supprimé, il faut aussi faire supprimer cette ligne CNAME.
