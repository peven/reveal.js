# Refactoring

![Refactoring](/slides/img/keep_calm_and_refactor.png)


## D&eacute;finition

> Refactoring is the process of changing a software system in such a way that it does not alter the external behavior of the code yet improves its internal structure. 
Martin Fowler

Implications:
- Le refactoring ne comprend aucune modification du système (global)
- Le refactoring n'est pas une r&eacute;ecriture 
- Un refactoring améliore le code dans un but précis.

Note:

- L'art d'améliorer sans risque la structure de code existant.
- Touche pas aux fonctionnalités existantes => éviter les régressions
- Part du code existant => La vérité est dans le code ! 
- Le refactoring a vocation a préparé le code pour accueillir de nouvelles fonctionnalités plus facilement, ou bien, atteindre un niveau de qualité manquant.  


## Enjeu

Le code existant: 
- n'est jamais parfait, 
- ni complétement adapté pour les nouvelles demandes 

Le refactoring doit nous permettre de remettre notre code dans un état satisfaisant pour affronter sereinement les nouvelles demandes d'évolution.   

Note: 

- Car la perfection n'est pas de ce monde, 
- et les contraintes externes peuvent avoir raison des meilleures intentions.
- Car le futur ne peut être anticiper  


## Quand doit-on refactorer ?

Le poids du code existant nous empêche d'avancer dans de bonnes conditions! 

Le code est difficile à modifier
- Personne ne le comprend
- Les impacts d’une modification ricochent à travers l’application 

La qualité est difficile à garantir
- Code difficilement testable
- Détection de Code Smells
 
Note:

- Lorsque vous vous dites : "Je ferai mieux de créer un nouveau module à côté du code existant." 
- Améliorer un code qui n'a pas besoin de changer => Perte de temps 


## Minimiser

> Premature optimization is the root of all evil.
Donald Knuth

- La solution la plus simple répondant au besoin connu aujourd’hui
- Cultivez la capacité de réagir au changement, sans l'anticiper

Note:

Rendez vous service: minimiser la comeplexité! Vos refactorings n'en seront que plus faciles. 

1. Une solution simple... pouvant être améliorer (refactorer) par la suite !
1. Méfiez vous de early optimisation


## TDD

![Red Green REFACTOR](/slides/img/redgreenrefactor.jpg)

Note:

- Refactoring = étape récurrente dans le TDD !
- Le code marche enfin, on a une vision clair du problème, on refactor vers une solution plus simple & pereine


## Code Legacy

Quelques définitions:
1. Code sans tests unitaires (Michael Feathers) 
1. Code dès qu'il est écrit.
1. Du code en production
1. Code dont les créateurs ne font pas parti de l'équipe.


## Refactoring du Code Legacy

1. Identifier les points de changement
1. Identifier les points de test associés
1. Casser les dépendances
1. Mise en place du harnais de tests
1. On applique des transformations et le refactoring
1. On valide nos modifications


## 1 Identifier les points de changement

Evolution du design

Code Smell


## Faire évoluer son design 

- Choix technique 
- Changement imprévu 
- Nouvelle stratégie

Note: 

- Nouvel ORM, ajout du Cache, …
- Modification d’une réglementation
- Expansion à l'International -> multi-langue, règlementations locales


## Code Smell

Bloaters - Long Method & Primitive Obsession
OO Abusers - Switch Statements
Change Preventers - Divergent Change & Shotgun Surgery
Dispensables - Comments & Duplicate Code
Couplers - Feature Envy & Inappropriate Intimacy
Test Smells


## 2 Identifier les points à tester

Tests unitaires, fonctionnels ?

Couverture ? La plus grande possible… mais ce n'est pas une garantie !


## Tests = Feedback

Qu’est ce que je veux savoir pour garantir la solidité de mon code ?


## 3. Casser Les Dépendances

Pour ramener le système sous test.
Plus gros frein aux tests !
Identifier les “Seams”, frontières entre les éléments du code

=> Crucial pour rendre les systèmes testables!


## Créer des doubles de test

Sale - Display 		

Sale - Interface - Display
					`- Fake Display


## 4. Ecrire les tests

Retour au TDD : 

** RED ** - GREEN - REFACTOR


## 5. Transformations & Refactoring

Transformations: 
- Extract Method
- Extract Class
- Extract Interface
- Hide Method
- Remove Middle Man
- Replace Conditional with Polymorphism
- Replace Constructor with Factory Method
- Change Value to Referencce


## N'oubliez pas les tests !

Refactoring des tests si nécessaire.

Test Code is just as important as Production Code 


## Pas d'ajout durant le refactoring !

On ajoute pas de nouvelles fonctionnalités durant le refactoring ! 
- Source de régression
- Pas couvert par les tests existant
- trop de modifications simultanées obscurcissent la source d'éventuelles régressions


## Rappel: Baby Steps


## Rappel : Use Tests


## D&eacute;fintion wikipedia

Le réusinage de code consiste à retravailler le code source d'un code informatique sans ajouter de fonctionnalité au logiciel ni corriger de bogues, mais en améliorant sa lisibilité pour simplifier sa maintenance, ou le rendre plus générique; on parle aussi de remaniement. …

En bref: Une réorganisation du code conservant les fonctionnalités inchangées, mais améliorant la maintenabilité et l’évolution.