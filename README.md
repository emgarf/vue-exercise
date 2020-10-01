# Front-end Exercise

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

J'aimerais ajouter une class active `:class="{ 'active': letter.active }"` quand je clique sur une lettre.<br/>
Mais ma fonction `addActiveOnLetter` ne fonctionne pas.<br/>
Pourtant dans la console, la clé `active` a bien été ajouté a l'objet sur lequel j'ai cliqué...

Une idée ? 🧐

Tu ne peux pas modifier l'array letters dans `data()`

Ensuite, tu peux modifier la fonction pour ajouter les fonctionalités suivantes:
- Déselectionner une lettre
- N'avoir qu'une seule lettre active

Une fois l'exercise terminé:
- Création d'une branche: `feature/`
- Création d'une pull request
- Ne pas push sur master
