# Initiation au Software Craftsmanship  _Le d&eacute;but du parcours_

formateur: [Peter Even]("mailto:peter.even@viseo.com") /
[@petervaneven]("http://twitter.com/petervaneven")



# Introduction


## Faisons connaissance

- Est-ce que tout le monde est programmeur? <!-- .element: class="fragment" data-fragment-index="1" -->
- Combien d'ann&eacute;es d'exp&eacute;rience en programmation? <!-- .element: class="fragment" data-fragment-index="2" -->
- Quels langages utilisez-vous? <!-- .element: class="fragment" data-fragment-index="3" --> 
- Quelles sont vos responsabilit&eacute;s au quotidien aujourd'hui? <!-- .element: class="fragment" data-fragment-index="4" --> 
- Ecrivez-vous des tests unitaires? <!-- .element: class="fragment" data-fragment-index="5" --> 
- Qu'attendez-vous de cette formation? <!-- .element: class="fragment" data-fragment-index="5" -->



## Qu'est ce que le Software Craftsmanship?

**Todo** <!-- .slide: data-background-image="Land-Of-Confusion.jpg" data- background-size="contain"
**data-background-repeat="no-repeat" font- color="#000000" -->


### Le Code _omnipr&eacute;sent_


### Coût de l'&eacute;chec


### M&eacute;thodes agiles


### Effet sur la **qualit&eacute;**



## Plan de la formation

1. Tests  
2. Clean Code 
3. Code Smells 
4. Refactoring



# La boîte &agrave; outil du Craftsman

![Toolbox](/img/toolbox.png)


## Tests : Overview


### Le coût du bug

Note: Le coût d'un bug croît exponentiellement plus il est découvert tardivement
- http://blog.celerity.com/the-true-cost-of-a-software-bug 
- https://www.isixsigma.com/industries/software-it/defect-prevention-reducing-costs-and-enhancing-quality/
- http://xbsoftware.com/blog/cost-bugs-software-testing/
- http://superwebdeveloper.com/2009/11/25/the-incredible-rate-of-diminishing-returns-of-fixing-software-bugs/


### Typologie

1. Tests **unitaires** <!-- .element: class="fragment" data-fragment-index="1" --> 
2. Tests d'**int&eacute;gration** <!-- .element: class="fragment" data-fragment-index="2" -->
3. Tests **fonctionnels** <!-- .element: class="fragment" data-fragment-index="3" -->
4. Tests de **non-régression** <!-- .element: class="fragment" data-fragment-index="4" -->
5. Tests d'**acceptance** <!-- .element: class="fragment" data-fragment-index="5" -->
5. Tests de **performance** <!-- .element: class="fragment" data-fragment-index="6" -->


### Propri&eacute;t&eacute;s d'un test unitaire

S&eacute;quence de code _**ex&eacute;cutable**_ et **automatisable** mesurant de manière **reproductible** le r&eacute;sultat d'un code **atomique** et **isol&eacute;**


### Effets d'un test unitaire

- Détection rapide d'erreurs
- Maintenance sécurisée
- Documentation technique
- Documentation fonctionnelle


### Nommer son test

- Classe de test => Contexte  
- Méthode => Comportement attendu
- Ne pas utiliser le mot *TEST* <!-- .element: class="fragment highlight-red" data-fragment-index="1"--> 

```csharp
public class WhenUserEditsEntry
{
	[Fact]
	public void ValidationShouldSucceedWhenTitleIsNotNullOrWhiteSpace()
	{
		...
	}
}
``` 
<!-- .element: class="fragment" data-fragment-index="2"--> 

Note: 
- classe de test représente l'élément ou comportement à tester
- méthode correspond au comportement attendu


### AAA

1. Arrange 
2. Act 
3. Assert 




### Code : What's in a name?



### Test-Driven Development (TDD)
