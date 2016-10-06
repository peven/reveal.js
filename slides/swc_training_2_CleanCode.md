# Clean Code

**_image_**

Note: 
1. Uncle Bob a popularisé la pratique du Clean Code au travers de ces deux livres Clean Code et Clean Coder. 
2. Développeur américain né en 1952  
3. Parmis les créateurs du manifeste Agile
4. SmallTalk & Java

## Overview

1. Clean Code
2. SOLID Principles
3. Yahtzee Kata


## Michael Feathers on Clean Code 

> *Clean code always looks like it was written by someone who cares.*
― @mfeathers


## Du code propre ?

* Du code structuré, rangé, cohérent & expressif
* Du code qui facilite la compréhension et l'utilisation

Note:

* Exemple de la paillasse du cuisinier

Ensemble de règles: 

- de programmation (objet)
- de nommage
- de documentation


## Pourquoi c'est important ?

- Développeur: 80% lecture / 20% écriture 
- La documentation est souvent incomplète, périmée, voir inexistente
- Code est partagé par les équipes
- En agile, il faut être préparer au changement

Note: 

1. Je ne parle même pas du support et des testeurs 


## Ratio Signal / Bruit

- l'Homme peut seulement conserver 7 éléments (+-2) dans sa mémoire court terme
- Trop d'informations simultannées perdent le lecteur
- Le bruit s'amplifie doucement au fil du temps. => rester vigilant!



# Nommage


## Exercice de Nommage

![Trousse](/slides/img/trousse_africaine.jpg)

- X
- Conteneur
- StyloCrayonsRegles&GommeManager
- => Trousse !

![Trousse](/slides/img/trousse_cuir.png)
![Trousse](/slides/img/trousse_japonaise.jpg)
![Trousse](/slides/img/trousse_de_secours.png)

Note:

* trousses?
* Trousse de secours?

## Nommer une classe

1. Un nom
2. Aussi spécifique que possible 
3. Responsabilité claire
4. Pas de suffixes superflus


## Ca suffixe !

* Object
* Manager
* Info
* Helper
* Executor
* Processor
* Utils
* Abstract
* ...

## Nommer une méthode

* Le nom doit suffire !
* Pas de nom générique (Do, Process, Execute ) 

=> ex: DocumentConverter.HtmlFromText(textFile);


## Appel à un ami !

Dans le doute, demandez à un collègue 



# Conditions

* Expressivité
* Concision


## Conditions non-non-positives 


## Magic Strings & Numbers


## Réduire la complexité 

* Expressive
* Extract Methode


## Comportement vs Enumération

* Polymorphisme pour injecter du comportement 
* plutôt que l'énumération de tous les comportements à un endroit


## Dictionaires

* Déplacer une liste de conditions dans une structure de données appropriée


## Concision

* Ternaire
* Linq / Lambdaj / jLinq / Pynq



# Functions


## 


# Conclusion


## Un investissement durable 

Cela fonctionne quelque soit
* le langage (objet)
* l'architecture
* les librairies



# Quotes

> *Good code is like a good joke. You should never have to explain it!*
― Venkat Subramaniam @venkat_s

> *If we continue to develop our technology without wisdom or prudence, our servant may prove to be our executioner.*
― Omar N. Bradley

> *Truth can only be found in one place: the code.*
― Robert C. Martin @unclebob

> *Make it work, make it right, make it fast.*
― Kent Beck

> *Leave the campground cleaner than the way you found it.* 
― Robert C. Martin @unclebob

> *Functions should do one thing. They should do it well. They should do it only.*
― Robert C. Martin @unclebob

> *Optimism is an occupational hazard of programming: feedback is the treament.*
― Kent Beck

> *Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it. And to make matters worse: complexity sells better.*
― Edsger W. Dijkstra