# Clean & Simple Code #
**_image_**

Note: 

1. Kent Beck <-> Simple Design : essentiel des pratiques dev XP 
1. Uncle Bob a popularis&eacute; la pratique du Clean Code au travers de ces deux livres Clean Code et Clean Coder. 
1. D&eacute;veloppeur am&eacute;ricain n&eacute; en 1952  
1. Parmis les cr&eacute;ateurs du manifeste Agile
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

* Du code structur&eacute;, rang&eacute;, coh&eacute;rent & expressif
* Du code qui facilite la compr&eacute;hension et l'utilisation

Note:

* Exemple de la paillasse du cuisinier

Ensemble de r&egrave;gles: 

- de programmation (objet)
- de nommage
- de documentation


## Pourquoi c'est important ?

- D&eacute;veloppeur: 80% lecture / 20% &eacute;criture 
- La documentation est souvent incompl&egrave;te, p&eacute;rim&eacute;e, voir inexistente
- Code est partag&eacute; par les &eacute;quipes
- En agile, il faut être pr&eacute;parer au changement

Note: 

1. Je ne parle même pas du support et des testeurs 


## Ratio Signal / Bruit

- l'Homme peut seulement conserver 7 &eacute;l&eacute;ments (+-2) dans sa m&eacute;moire court terme
- Trop d'informations simultann&eacute;es perdent le lecteur
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
2. Aussi sp&eacute;cifique que possible 
3. Responsabilit&eacute; claire
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


## Nommer une m&eacute;thode

* Le nom doit suffire !
* Pas de nom g&eacute;n&eacute;rique (Do, Process, Execute ) 

=> ex: DocumentConverter.HtmlFromText(textFile);


## Appel &agrave; un ami !

Dans le doute, demandez &agrave; un coll&egrave;gue 



# Conditions

> If I had more time I would have written a shorter letter. Blaise Pascal

* Expressivit&eacute;
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

* Pr&eacute;f&eacute;rez les formulations positives
* Impr&eacute;cision des ensembles flous


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

* Facilit&eacute; au changement
* Garanti de la compilation


## R&eacute;duire la complexit&eacute; 

```python
if date.before(SUMMER_START) and date.after(SUMMER_END):
    charge = quantity * winterRate + winterServiceCharge
    if WINTER_SALE_START < date < WINTER_SALES_END:
        charge = charge * 0.7    
else:
    charge = quantity * summerRate
```

* Favoriser une m&eacute;thode
* Extraire m&eacute;thode


## Comportement vs Enum&eacute;ration

* Polymorphisme pour injecter du comportement 
* plutôt que l'&eacute;num&eacute;ration de tous les comportements &agrave; un endroit


## Dictionaires

* D&eacute;placer une liste de conditions dans une structure de donn&eacute;es appropri&eacute;e


## Concision

* Ternaire
* Linq / Lambdaj / jLinq / Pynq



# Functions

> *Functions should do one thing. They should do it well. They should do it only.*
― Robert C. Martin @unclebob


## Pourquoi cr&eacute;er une fonction?

* Eviter la duplication
* R&eacute;duire l'indentation du code
* Clarifier l'intention d'un code 
* S&eacute;parer diff&eacute;rentes op&eacute;rations

Note:

* dup: Mutualiser pour r&eacute;utiliser & &eacute;viter les disparit&eacute;s
* ind: R&eacute;duire la complexit&eacute; cyclomatique
* int: Introduire des concepts de plus haut niveau, r&eacute;duire le nombre d'&eacute;l&eacute;ments locaux.
* sep: Diviser pour mieux r&egrave;gner - &eacute;viter les effets de vase communicants


## M&eacute;triques

Uncle Bob, dit qu'une fonction ne devrait :
- rarement faire plus de 20 lignes
- quasi jamais plus de 100 lignes,
- pas avoir plus de 3 param&egrave;tres. 



# Exceptions

3 types d'exceptions:
* Fatale
* G&eacute;rable
* N&eacute;gligeable

Note:

- fat: ressources obligatoires dysfonctionnant. Incapacit&eacute; de l'app &agrave; se rattraper gracieusement.
- ger: une ou plusieurs solutions existent : rejeu, operation alternative
- neg: pas d'incidence sur l'application. (code in&eacute;l&eacute;gant dans une api de plus bas niveau)


## Rien sous le tapis!

* Bubble exceptions to competent level
* Don't handle exception if you can't revert to stable state
* Last resort, handle at topmost level and shutdown app or abort web call 



# Classes


## <New Class>

* Nouveau concept
* Coh&eacute;sion faible
* R&eacute;utilisation
* R&eacute;duire la complexit&eacute;

Note:

**r&eacute;duire complexit&eacute;**: 
- diminuer le nombre d'&eacute;l&eacute;ments (coh&eacute;sion) 
- encapsuler des variables dans une structure coh&eacute;rente


## Coh&eacute;sion & Couplage 

* Coh&eacute;sion *forte*
    - Regroupement fonctionnel
    - Même niveau de détail

* Couplage *faible*
    - Minimiser dépendances 


## Soyez protecteur 

Exposez le minimum nécessaire


## Primitive Obsession

```cs
// Only uses primitives ...
public void SaveUser(int id, string nom, string prénom, string adresse, string téléphone);

// When an object could easily sum it up !
public void SaveUser(User user);
``` 


## Principe de proximité

Conserver les éléments liés à proximité


## Table des matières

Le code collapsed se lit comme un résumé



# Commentaires

> redondance / évidence / péremption / inutile


## To comment or not to comment

* Résumé
* Code désactivé
* Avertissement
* Clarification

Note: 

* Résumé
    - Duplication  
    - Approximation
    - Vision erronée/périmée
* Code désactivé
    - Zombie code => Delete
* Avertissement : Todo/Warning
    - Dette technique
* Clarification
    - Signe de code trop long ?


## Questions à se poser

- Arrivez-vous à exprimer l'intention dans le code?
- Est-ce que le commentaire est un déodorant ?
- Sa place est dans le code source?



# Simple Design

> *Make it work, make it right, make it fast.*
― Kent Beck


## 4 rules of Simple Design

* Valide les tests
* Exprime clairement son intention 
* Contient aucune duplication
* Minimise le nombre d'&eacute;l&eacute;ments

Note:

**ATTENTION**: Minimiser tant qu'on n'enfreint pas la seconde r&egrave;gle ! 



# Conclusion

> *Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it. And to make matters worse: complexity sells better.*
― Edsger W. Dijkstra


## La v&eacute;rit&eacute; est dans le code

* Le code est majoritairement lu
* Le code est la seule documentation &agrave; jour
* Le bruit est l'origine de mauvaises implémentations & bugs


## Clean Code

* Clair
* Concis
* Expressif
* Flexible
* Adaptable


## Un investissement durable 

Cela fonctionne quelque soit
* le langage (objet)
* l'architecture
* les librairies


## Des pratiques partagées !

* Documenter des standards
* Pair Programming / Mob Programming 
* Code Reviews 
* Outils de suivi de la qualité du code



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

> Perfection is not when there is no more to add, but no more to take away. Antoine de Saint Exup&eacute;ry

> Conciseness is the sister of talent. Anton Chekhov

> The ability to simplify means to eliminate the unnecessary so that the necessary may speak. Hans Hofmann

> Less is more. Stephen Sondheim
