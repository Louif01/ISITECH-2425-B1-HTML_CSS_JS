# énoncé

- <u>**Questions sur la Structure**</u> :
  Dans l'exercice du gestionnaire de films, pourquoi a-t-on utilisé la propriété flex: 1 sur la classe .input-zone ? Quel effet cela produit-il sur la mise en page ?

```
Cela permet de modifier ses dimensions, la barre de sélection "Genre" s'agrandit si on enlève le flex 1 ça l'a réduit.
```

- <u>**Questions sur le JavaScript**</u> :
  Expliquez pourquoi on utilise selectedIndex = 0 pour réinitialiser le select de genre au lieu de value = "" comme pour les autres inputs ?

En résumé, selectedIndex = 0 est utilisé pour les champs de sélection afin de revenir à la première option, tandis que value = "" est utilisé pour les champs de saisie pour les vider. Cela permet de réinitialiser correctement chaque type de champ à son état initial.


- <u>**Questions de Modification**</u> :
  Comment modifieriez-vous le code pour que les films dont l'année est antérieure à 2000 apparaissent en italique dans le tableau ?

```css
 .italic {
        font-style: italic;
      }
```

```script
if(parseInt(inputAnnee.value) < 2000) {
          cellTitre.classList.add("italic");
        }
```

