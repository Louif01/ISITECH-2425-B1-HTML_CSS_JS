# Enonce

- Questions sur le CSS :
  "Expliquez l'utilité de la propriété flex-wrap: wrap dans la classe .task-form. Que se passe-t-il si on la retire ?"

La propriété flex-wrap: wrap en CSS est utilisée pour contrôler le comportement des éléments flexibles lorsqu'ils ne tiennent pas dans une seule ligne. Par défaut, les éléments flexibles sont placés sur une seule ligne. Si on le retire tous les éléments se mettront l'un à côté de l'autre pour ne tenir sur qu'une seule ligne.


- Questions sur la Logique :
  "Dans la fonction ajouterTache(), expliquez la condition qui vérifie la priorité haute et ajoute la classe CSS. Comment pourriez-vous l'étendre pour gérer différemment les priorités moyennes ?"

  La condition vérifie si la valeur que l'on sléectionne dans Priorité soit égal à Haute si c'est le cas alors il va l'afficher en rouge.

Pour l'étendre on tape ce code :

```js
if (selectPriorite.value === "Haute") {
          cellPriorite.classList.add("priorite-haute");
        }

        if (selectPriorite.value === "Moyenne") {
          cellPriorite.classList.add("priorite-moyenne");
        }

        if (selectPriorite.value === "Basse") {
          cellPriorite.classList.add("priorite-basse");
        }
```

```cs
  .priorite-haute {
        color: #e53e3e;
        font-weight: bold;
      }
      
      .priorite-moyenne {
        color: orange;
        font-weight: bold;
      }

      .priorite-basse {
        color: green;
        font-weight: bold;
      }
```


- Questions sur l'Amélioration :
  "Comment ajouteriez-vous une validation pour empêcher l'ajout d'une tâche si la date limite est antérieure à la date du jour ?"

On créé deux variables, dateLimite et dateAujourdhui une pour récupérer la date que l'on va rentrée et une autre pour récupérer la date du jours.
On va aussi reset l'heure à 0 0 0 0 pour ne comparé que la date sans l'heure.
Ensuite on va mettre en place une condition pour dire : si la date que l'on va rentrer est infèrieur à celle du Jour J alors il va faire apparaître une alerte pour expliquer que ce n'est pas possible et le return sert à ne pas ajouter ce qu'on a rentré.

  Il faut taper ce code :

  ```js
    var dateLimite = new Date(inputDate.value);
    var dateAujourdhui = new Date();
    dateAujourdhui.setHours(0, 0, 0, 0);

        if (dateLimite < dateAujourdhui) {
          alert("La date limite doit être supérieure ou égale à la date d'aujourd'hui.");
          return;
        }
```