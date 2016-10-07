# Clean & Simple Code

**_image_**

Note: 

1. Kent Beck <-> Simple Design : essentiel des pratiques dev XP 
1. Uncle Bob a popularisé la pratique du Clean Code au travers de ces deux livres Clean Code et Clean Coder. 
1. Développeur américain né en 1952  
1. Parmis les créateurs du manifeste Agile
1. SmallTalk & Java

## Overview

1. Clean Code
1. Simple Design
1. SOLID Principles
1. Yahtzee Kata


## Clean Code 

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



# Nommage #

> What's in a name? that which we call a rose 
> By any other name would smell as sweet.
― William Shakespeare, Romeo and Juliet 

> Call him Voldemort, Harry. Always use the proper name for things. Fear of a name increases fear of the thing itself.
― J.K. Rowling, Harry Potter and the Sorcerer's Stone 

> I confused things with their names: that is belief.
― Jean-Paul Sartre, The Words 

> If names be not correct, language is not in accordance with the truth of things.
― Confucius, The Analects of Confucius 

> Names and attributes must be accommodated to the essence of things, and not the essence to the names, since things come first and names afterwards.
― Galileo Galilei, Discoveries and Opinions of Galileo 


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

> If I had more time I would have written a shorter letter. Blaise Pascal

* Expressivité
* Concision


## Conditions non-non-positives 

```javascript
function doSomething(entity) {

    if (!entity.isNotSelected && client!=null) {
        ...
    }

    if (!entity instanceof Person) {
        ...
    }
    else {
        ...
    }   
}
```

* Préférez les formulations positives
* Imprécision des ensembles flous


## Magic Strings & Numbers

```Java
public void Initialize(Person person, int level, Date date) 
{
    if (level != 6)
        person.Title = "Employee";
    else
        person.Title = "Chief Dictator"; 

    if (person.Title == "Employee") {
        ...
    }
}
```

* Facilité au changement
* Garanti de la compilation


## Réduire la complexité 

```python
if date.before(SUMMER_START) and date.after(SUMMER_END):
    charge = quantity * winterRate + winterServiceCharge
    if WINTER_SALE_START < date < WINTER_SALES_END:
        charge = charge * 0.7    
else:
    charge = quantity * summerRate
```

* Favoriser une méthode
* Extraire méthode


## Comportement vs Enumération

* Polymorphisme pour injecter du comportement 
* plutôt que l'énumération de tous les comportements à un endroit


## Dictionaires

* Déplacer une liste de conditions dans une structure de données appropriée


## Concision

* Ternaire
* Linq / Lambdaj / jLinq / Pynq



# Functions

> *Functions should do one thing. They should do it well. They should do it only.*
― Robert C. Martin @unclebob


## Pourquoi créer une fonction?

* Eviter la duplication
* Réduire l'indentation du code
* Clarifier l'intention d'un code 
* Séparer différentes opérations

Note:

* dup: Mutualiser pour réutiliser & éviter les disparités
* ind: Réduire la complexité cyclomatique
* int: Introduire des concepts de plus haut niveau, réduire le nombre d'éléments locaux.
* sep: Diviser pour mieux règner - éviter les effets de vase communicants


## Métriques

Uncle Bob, dit qu'une fonction ne devrait :
- rarement faire plus de 20 lignes
- quasi jamais plus de 100 lignes,
- pas avoir plus de 3 paramètres. 



# Exceptions

3 types d'exceptions:
* Fatale
* Gérable
* Négligeable

Note:

- fat: ressources obligatoires dysfonctionnant. Incapacité de l'app à se rattraper gracieusement.
- ger: une ou plusieurs solutions existent : rejeu, operation alternative
- neg: pas d'incidence sur l'application. (code inélégant dans une api de plus bas niveau)


## Rien sous le tapis!

* Bubble exceptions to competent level
* Don't handle exception if you can't revert to stable state
* Last resort, handle at topmost level and shutdown app or abort web call 


# Simple Design

> *Make it work, make it right, make it fast.*
― Kent Beck


## 4 rules of Simple Design

* Valide les tests
* Exprime clairement son intention 
* Contient aucune duplication
* Minimise le nombre d'éléments

Note:

**ATTENTION**: Minimiser tant qu'on n'enfreint pas la seconde règle ! 



# Classes


## <New Class>

* 

# Conclusion

> *Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it. And to make matters worse: complexity sells better.*
― Edsger W. Dijkstra


## Clean Code ???

* Clair
* Expressif
* Flexible
* Adaptable


## La vérité est dans le code

* Le code est majoritairement lu
* Le code est la seule documentation à jour
* Le bruit du code est à l'origine de bugs


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


> *Leave the campground cleaner than the way you found it.* 
― Robert C. Martin @unclebob

> Learn from the mistakes of others. You can never live long enough to make them all yourself.
― Groucho Marx

> Those are my principles, and if you don't like them...well I have others. Groucho Marx

> The best sentence? The shortest. Anatole France

> Perfection is not when there is no more to add, but no more to take away. Antoine de Saint Exupéry

> Conciseness is the sister of talent. Anton Chekhov

> The ability to simplify means to eliminate the unnecessary so that the necessary may speak. Hans Hofmann

> Less is more. Stephen Sondheim
