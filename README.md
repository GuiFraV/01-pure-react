# Introduction à React : useState et useEffect

Ce code est un exemple simple pour comprendre les hooks `useState` et `useEffect` de React dans un fichier HTML. C'est une première étape pour ceux qui débutent avec React.

## Description

Le code HTML intègre les bibliothèques React et ReactDOM depuis un CDN. Il contient une fonction `App` qui est un composant React. Cette fonction utilise les hooks `useState` et `useEffect` pour afficher l'heure actuelle et la mettre à jour chaque seconde.

### useState

Le hook `useState` est utilisé pour définir un état local dans le composant. Dans cet exemple, il est utilisé pour stocker l'heure actuelle :

```javascript
const [time, setTime] = React.useState(new Date().toLocaleTimeString());
```

- **time** : est la valeur actuelle de l'état.
- **setTime** : est une fonction qui permet de mettre à jour cette valeur.


### useEffect

Le hook `useEffect` permet d'exécuter des effets secondaires dans les composants. Dans cet exemple, il est utilisé pour mettre à jour l'heure toutes les secondes :


```javascript
React.useEffect(function(){
    setInterval(function(){
        setTime(new Date().toLocaleTimeString())
    }, 1000)
}, []);
```

L'effet utilise `setInterval` pour mettre à jour l'heure chaque seconde. Le tableau vide `[]` passé en second argument signifie que l'effet sera exécuté une seule fois après le rendu initial du composant.

## Comment ça marche ?

Lorsque la page est chargée, le composant `App` est rendu dans la div avec l'id `root`. Le composant affiche un message de bienvenue avec l'heure actuelle. Grâce à `useEffect`, l'heure est mise à jour toutes les secondes.

## Conclusion

Cet exemple est une excellente introduction aux concepts de base de React. Si vous débutez avec React, n'hésitez pas à expérimenter avec ce code pour mieux comprendre comment fonctionnent les hooks et les composants.
