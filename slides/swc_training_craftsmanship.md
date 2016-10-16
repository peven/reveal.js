
## Software Craftsmanship

*Prolongement du développement applicatif Agile*


### Agile Manifesto

> Individuals and interactions over processes and tools <!-- .element: class="fragment highlight-current-blue" data-fragment-index="1" -->

> Working software over comprehensive documentation <!-- .element: class="fragment highlight-current-blue" data-fragment-index="2" -->

> Customer collaboration over contract negotiation <!-- .element: class="fragment highlight-current-blue" data-fragment-index="3" -->

> Responding to change over following a plan <!-- .element: class="fragment highlight-current-blue" data-fragment-index="4" -->

Note: 

En **2001**, 17 experts ont fig&eacute; les **4 valeurs** & **12 principes** de l'agilit&eacute;.

1. Le client et le produit au centre
1. Processus itératif évite l'effet tunnel & valorise la réactivité
1. Casser les longues chaines de décision et rapprocher les intervenants 

Forcément d'accord après un projet en V raté. 
Cependant la réalité du terrain ne correspond pas.


### La gueule de bois Agile

![Post it nightmare](/slides/img/postItNightmare.jpg)

Note: 

Mirage de l'eldorado des post-its: Les projets IT échouent toujours!

Le problème c’est que le « Working Software » a été pris au pied de la lettre

Pas mal de projet et d’équipe utilisant souvent SCRUM et qui se sont trop concentré sur la vitesse de développement et le working software 
se sont réveillé avec une sacré gueule de bois

Car sans s’investir sur la qualité, le code a les mêmes problèmes qu’avant l’agilité
Un code peu maintenable, compliqué, on sait pas quoi en faire voir même comment vivre avec


Changement de méthodologie sans changement de culture:
- Rythme insoutenable 
- Qualité médiocre des projets 

Effet de mode nuisibles:
- Business des coachs et certifications agiles


### Temps

![Spirale infernale](/slides/img/time.jpg)

Note:

Le problème c’est qu’on a une mauvaise relation au temps.

Le nombre de fois où j'ai entendu : "on a pas le temps de faire des tests".
Par contre on a le temps de faire des semaines de test pour trouver tous les bugs avant la livraison ? 

- On ne trace pas précisement le temps pris par la correction d'un bug.
- On pas de métriques comparatives pour un bug.   
- Les développeurs sont des perfectionnistes et prennent les bugs comme des remises en question : minimise le temps de résolution, résolution sur temps perso ou maquillage du temps 


### Le principe oublié

> Continuous attention to technical excellence and good design
**enhances** <!-- .element: class="fragment highlight-red" data-fragment-index="1" -->
agility.  

Devrait être: 

> Continuous attention to technical excellence and good design
**saves** <!-- .element: class="fragment highlight-green" data-fragment-index="2" -->
agility.  

Note:

enhances -> améliore : manque l'aspect nécessaire d'accorder de l'attention à excellence technique et au bon design 


### La menace du code

![Invisible threat](/slides/img/hiddenThreat.png)

Note: 

1. Le time to market, force du modèle agile, explose quand la qualité du code devient trop mauvaise. 
1. Les imperfections du code freinent l'ajout ou la modification de fonctionnalités
1. Mais pourquoi écrit-on du mauvais code ? et pourquoi autant ?! 


### Inconscience du développeur ?!

![Crazy Coder](/slides/img/Fotolia_56962791_M.jpg)

Note:

1. Est-ce que les développeurs sont insconscients ?
1. On se fait du tort à écrire du mauvais code, car il viendra nous hanter
1. On entend, c'est ce que me demande mon cdp... => Pas satisfaisant ? Sommes nous de simples exécutants ?


### Constat

1. Le code est partout.
1. Demain tout sera code.
1. Le nombre de développeurs croit de moitié tous les 10 ans
1. Confierez-vous votre vie à une voiture automatique? 
1. Confierez-vous votre opération à coeur ouvert à un programme ?


### Nos Valeurs ?

![Lost](/slides/img/Land-Of-Confusion.jpg)

Note: 

1. Est-ce que le développeur est un ingénieur au même titre qu'un autre ? Ou un simple exécutant ?
1. Le rôle de développeur porte encore une connotation péjorative. => Geek introverti incapable de travailler en équipe
1. Faut-il légiférer et normer les tâches du développeur ? 
1. Faut-il des certifications de qualité pour les développeurs ?
1. Autre solution ?


### Take back control 

![Uncle Bob Needs You](/slides/img/uncle-bob.jpg)

**Become a Craftsman!**

Note:

Les devs doivent prendre le controle de leur destinée ! (uncle bob)

Tête de ligne du mouvement software craftsmanship, uncle bob faisait parti des signataire du manifeste agile.

1. Une catastrophe informatique nous pend au nez. Et ce jour là, les politiques et les juges viendront légiférer sur comment on doit développer.
1. Seule alternative: les développeurs doivent se prendre en main et améliorer leurs pratiques pour plus de qualité.
1. Craftsman = Artisan. Un professionnel passionné par son travail, cherchant sans cesse à perfectionner son art.

Il propose des principes de dev du Clean Code et certains autre pour améliorer la qualité de notre code. ce sont devenus des standards du swc.   


### Software Craftsmanship Manifesto

> Not only working software,
but also well-crafted software

> Not only responding to change,
but also steadily adding value

> Not only individuals and interactions,
but also a community of professionals

> Not only customer collaboration,
but also productive partnerships

Note:

le manifeste du SWC vient en complément du manifeste Agile. Ne remet pas en cause l'agilité !

On mets l'accent sur les éléments oubliés ou pas suffisamment mis en avant, et on promeut un nouvel état d'esprit du développeur.

1. Une voiture qui roule aujourd'hui n'est pas suffisant, il faut qu'elle roule demain. 
1. Pas uniquement en réaction, mais une véritable vision sur le long terme. Pas de rustines! 
1. Communauté de professionnels échangeant les bonnes pratiques et propageant la culture de l'apprentissage
1. Collaboration bi-directionnelle: même si le client est primordial, il n'est pas roi. (président ?)


### Les pratiques XP

![Xp Practices](/slides/img/xp_practices.jpg)

Note:

XP Values
- Communication
- Simplicity
    + “What is the simplest thing that could possibly work?”
- Feedback
    + Understanding what has changed & what we are getting wrong
    + Includes opinions & observations on what turned out to be complicated, hard to do, hard to get right, etc.
- Courage
    + a bias toward action
- Respect
    + care about the team members
    + care about he project


### Autres pratiques 

- Clean Code & SOLID
- Domani Driven Design
- Mob Programming
- Coding dojos
- Brown bag lunch


### Les bonnes pratiques...

...ne sont bonnes que jusqu'au jour où l'on en trouve de meilleurs.

Note: 

Ne soyez pas dogmatique! Un jour il y aura de meilleures pratiques que le TDD & pair progamming.


###   

Le but du Software Craftmanship n'est pas de suivre les pratiques, ou d'avoir du beau code, 
mais de délivrer continuellement de la valeur au travers d'applications bien conçues


### Software Craftsman

- professionnel
- responsable
- pragmatique
- résolu
- mentor (généreux)
- mentee (humble)

Note:

- prof : se gardant à jour dans son domaine
- resp : ne livrera pas un produit en deça du niveau de qualité acceptable
- prag : conscient que chaque contexte dicte le niveau d'acceptabilité
- résolu : capable de défendre sa position dans l'adversité
- mentor : ??? 
- mentee : ???

Ca fait beaucoup. Certains trouvent élitiste ce mouvement.
Ce n'est pas vrai ! C'est simplement un appel aux développeurs soucieux de progresser et de bien faire leur travail.
Un phare au milieu de la nuit...
