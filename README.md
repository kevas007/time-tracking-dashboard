![Preview](./exo-ressources/design/desktop-preview.jpg)

## Le challenge

Le challenge est de créer un dashboard similaire à celui des exemples fournis. Vous trouverez les ressources habituelles (design, style guide) dans le dossier `exo-ressources`.

Votre code devrait :

- Utiliser des components intelligemment pour subdiviser la page et éviter les répétitions
- Utiliser du SASS/SCSS pour le style
- **Bonus** Recevoir les datas depuis le fichier `data.json` plutôt que directement dans `data(){}`

L'utilisateur devrait être capable de :

- Voir les états "hover" de tous les éléments interractifs de la page
- Changer entre journalier, mensuel et annuel

### Comportement attendu

- Le texte pour la période précédente devrait changer en fonction de la timeframe. "Hier" pour journalier (ex : `Hier - 2h`), "La semaine passée" pour hebdomadaire, "Le mois passé" pour mensuel.

**Bonne chance !** 👾

_ps : commencez par un_ `npm i`