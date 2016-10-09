# Code Smells

![Toolbox](/slides/img/smelly.jpg)


## Comme une odeur... 

>A code smell is a surface indication that usually corresponds to a deeper problem in the system. - Martin Fowler


### Type of Code Smells

|                   |
|:------------------|
| Bloaters          |
| OO Abusers        |
| Change Preventers |
| Dispensables      |
| Couplers          |
|                   |



## Les Gonflants

| Bloaters            |
|:--------------------|
| Long Method         |
| Large Class         |
| Primitive Obsession |
| Long Parameter List |
| Data Clumps         |
|                     |

Note: 

Font grossir le code dans des proportions diminuant la lisibilité et la flexibilité.  


## Bloaters > Long Method

-
-

**Corriger**

-
-

Note:


## Bloaters > Large Class

-
-

**Corriger**

-
-

Note:



## Les Casseurs

| Object-Oriented Abusers         |
|:--------------------------------|
| Switch Statements               |
| Temporary Field                 |
| Refused Bequest                 |         
| Alt. Classes w/ dif. Interfaces |
|                                 |

Note:

Contraires aux valeurs des langages objets
- encapsulation
- polymorphisme
- héritage


## OO Abusers > Switch Statements

-
-

**Corriger**

-
-

Note:



## Les Bureaucrates

| Change Preventers                |
|:---------------------------------|
| Divergent Change                 |
| Shotgun Surgery                  |         
| Solution Sprawl                  |
| Parallel Inheritance Hierarchies |
|                                  |

Note: Responsabilité répandu à travers le code empêchant la modification 


## Change Preventers > Shotgun Surgery

-
-

**Corriger**

-
-

Note:



## Les Superflus

| Dispensables           |
|:-----------------------|
| Lazy Class             |
| Data Class             |
| Duplicate Code         |
| Dead Code              |
| Speculative Generality |
|                        |

Note: 

Signe de code inutile
- Enrichir les éléments  
- ou supprimer le code (middle man)  


## Dispensables > Data Class

- Aucune méthode
- Bcp d'autres classes en dépendent
    - ViewModel ou DTO ?

**Corriger**

- Move / Extract Method 
- Hide Method / Remove Setting Method
- Encapsulate Field / Collection

Note: 

Data classes doivent se responsabiliser pour justifier leur existence. 



## Les Pots de Colle 1/2

| Couplers                  |
|:--------------------------|
| Artificial Coupling       |
| Feature Envy              |
| Inappropriate Intimacy    |
| Incomplete Library Class  |
| |

Note: 

Classes difficiles à modifier individuellement du à des dépendances non nécessaire.


## Les Pots de Colle 2/2

| Couplers                  |
|:--------------------------|
| Indecent Exposure         |
| Hidden Dependencies       |
| Message Chains            |
| Middle Man                |
| Tramp Data                |
|                           |


## Couplers > Feature Envy

-
-

**Corriger**

-
-

Note:


## Couplers > Inappropriate Intimacy

-
-

**Corriger**

-
-

Note:


## Couplers > Hidden Dependencies

-
-

**Corriger**

-
-

Note:



## R&eacute;f&eacute;rences

- Article
    - [Code Smell](http://martinfowler.com/bliki/CodeSmell.html), Martin Fowler

- Books
    - Refactoring, Martin Fowler 
    - Clean Code, Robert C Martin