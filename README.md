# Technical Interview

# Questions

  * Décris-moi ton parcours personnel, professionnel, education

  * Tes objectifs, ce que tu recherches au sein d'une entreprise ?

  * Les technos et langages  que tu as eu l'expérience d'utiliser, celles que tu aimes et celles que tu voudrais essayer ?

  * Plutôt backend ou frontend ? Expériences en développement mobile ?

  * Quelques exemples de design patterns ?

    * Singleton, Factory, Builder, Strategy, Publish/Subscribe...

  * Expérience Typescript ?

  * différence entre var, let et const ?

    * var fait parti du scope global alors que let et const du scope du block, let peut etre réassignée, const non

  * Nouveautés de ES6 (Ecmascript 6)?

    * deconstruction, arrow function, paramètres par defaut, opérateur spread, opérateur rest, for of

  * C'est quoi une promesse ?

    * C'est un objet qui peut peut être retourner une valeur dans le futur

  * Quels sont les états possibles d'une promesse ?

    * en cours, resolue, rejectée

  * A quoi servent les fonctions de l'objet Array map, filter, reduce ? Quel est la différence entre map et forEach ? Peux tu me donner d'autre fonction de l'objet Array ? 

  * différence entre l'opérateur == et l'opérateur === ? 

    * le premier check l'égalité, le second l'égalité et les types

  * Comment faire une deepcopy d'un objet ? 
    
    * Object.assign, JSON.parse(JSON.stringify()), spread operator

  * Différence entre deepcopy et shallowcopy ?

    * deepcopy va copier tout et garder aucune référence alors qu'une shallowcopy va garder les mêmes références pour les objets nested

  * As-tu déjà utilisé Express pour le backend ? Qu'est ce que c'est ? Quel est le principe des middlewares ?

    * Express est un framework pour nodejs permettant de développer des serveurs webs/api. Un middleware est une fonction
      prenant en paramètre 3 fonctions, request, response et next, la requete quand elle est recue passe à travers les middlewares
      qui peuvent modifier la requete et la reponse et appeler next pour passer la requete et la reponse aux prochains middlewares
      lorsque il n'y plus de middlewares ou que la reponse est explicitement renvoyée, la reponse est renvoyée à l'envoyeur de la requete

  * Donne moi un cas d'utilisation d'un middleware

    * par exemple pour implementer de gestion de droits sur une route

  * C'est quoi une API REST ? Sa particularité ?

    * c'est des routes que l'ont va mettre à disposition sur un serveur web pour effectuer des actions ou récuperer des données
      la particularité est quelle est sans état

  * As-tu déjà utilisé React ou Vue ? C'est quoi ?

    * Ce sont des bibliothéques Javascript frontend pour construire des interfaces utilisateur
    
  * React

    * Qu'est ce qu'un component ? 

      * Un bout de code représentant un élément de la page qui retourne du HTML et/ou d'autres components

    * La méthode la plus importante d'un component (Class) ?

      * La méthode render qui retourne le rendu HTML du component, qui est appelée à chaque fois que les props ou le state change

    * Cycle de vie d'un component ?

      * mount, render, update, unmount

    * C'est quoi Redux ?

      * Bibliothèque de management de state

    * Cycle de vie d'une mise à jour de l'état ?

      * dispatch des actions qui passe dans les reducers qui vont mettre à jour les stores

    * Est-ce toujours nécessaire ?

  * Vue

    * Vuex ? Nécessaire ?

  * Frameworks CSS ?

    * bootstrap, bulma, antdesign...

  * Database

    * relational database ? 

      * MySQL, Postgres, MariaDB, SQLite...

    * non relational ? 

      * MongoDB, Redis, Cassandra...


# Test

  * implémenter la suite de fibonacci en javascript

  ```
  fonction fibo(n)
     si n = 0 alors renvoyer 0
     sinon si n = 1 alors renvoyer 1
     sinon renvoyer fibo(n - 1) + fibo(n - 2)

  implementer la fonction retourner une suite de 0 à 20 sous la forme: '0, 1, 1, 2, ...'
  ```
  Particularité de cette fonction ? C'est quoi une fonction récursive ?

  * fizzbuzz

  ```
  Pour x de 1 à 100
  Si x divisble par 3 et 5 (15) => FizzBuzz
  Si x divisible par 3 => Fizz
  Si x divisible par 5 => Buzz
  Sinon => x
  ```

  * Output de ces lignes ? 

  ```
  console.log("0 || 1 = "+(0 || 1));
  console.log("1 || 2 = "+(1 || 2));
  console.log("0 && 1 = "+(0 && 1));
  console.log("1 && 2 = "+(1 && 2));
  ```
  ```
  0 || 1 = 1
  1 || 2 = 1
  0 && 1 = 0
  1 && 2 = 2
  ```
  
  * Créer une fonction pour print un escalier de # pour une hauteur de  x marches 
  ```
  Pour x = 4 l'outpur sera :
     #
    ##
   ###
  ####
  ```
  
  ```
  function staircase(x) {
    for(let i = 1; i <= x; i++) {
      console.log(('#'.repeat(i)).padStart(x))
    }
  }
  ```
