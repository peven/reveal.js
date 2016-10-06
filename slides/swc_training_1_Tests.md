


# La boîte &agrave; outil du Craftsman

![Toolbox](/slides/img/Fotolia_93525027_S.jpg)


## Tests : Overview


### Le coût du bug

Note: 

Le coût d'un bug croît x² plus il est d&eacute;couvert tardivement
- http://blog.celerity.com/the-true-cost-of-a-software-bug 
- https://www.isixsigma.com/industries/software-it/defect-prevention-reducing-costs-and-enhancing-quality/
- http://xbsoftware.com/blog/cost-bugs-software-testing/
- http://superwebdeveloper.com/2009/11/25/the-incredible-rate-of-diminishing-returns-of-fixing-software-bugs/


### Typologie

1. Tests **unitaires** <!-- .element: class="fragment" data-fragment-index="1" --> 
2. Tests d'**int&eacute;gration** <!-- .element: class="fragment" data-fragment-index="2" -->
3. Tests **fonctionnels** <!-- .element: class="fragment" data-fragment-index="3" -->
4. Tests de **non-r&eacute;gression** <!-- .element: class="fragment" data-fragment-index="4" -->
5. Tests d'**acceptance** <!-- .element: class="fragment" data-fragment-index="5" -->
6. Tests de **performance** <!-- .element: class="fragment" data-fragment-index="6" -->

Note: 

- unitaires: &eacute;l&eacute;ment fonctionne correctement seul
- int&eacute;gration: &eacute;l&eacute;ments fonctionnent correctement ensembles
- fonctionnels: &eacute;l&eacute;ments r&eacute;pondent aux sp&eacute;cifications &eacute;tablies pr&eacute;alablement
- non-regression: syst&agrave;me valide selon les jeux de tests pr&eacute;-&eacute;tablis 
- acceptance: syst&agrave;me r&eacute;pond aux attentes des utilisateurs finaux
- performance: &eacute;l&eacute;ment, ou syst&agrave;me entier, r&eacute;pond aux contraintes de performances d&eacute;finies  

### Propri&eacute;t&eacute;s d'un test unitaire

S&eacute;quence de code _**ex&eacute;cutable**_ et **automatisable** mesurant de mani&agrave;re **reproductible** le r&eacute;sultat d'un code **atomique** et **isol&eacute;**


### Effets d'un test unitaire

- D&eacute;tection rapide d'erreurs
- Maintenance s&eacute;curis&eacute;e
- Documentation technique
- Documentation fonctionnelle


### Nommer son test

- Classe de test => Contexte  
- M&eacute;thode => Comportement attendu
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
- classe de test repr&eacute;sente l'&eacute;l&eacute;ment ou comportement à tester
- m&eacute;thode correspond au comportement attendu


### Organiser ses tests 

1. Arrange 
2. Act 
3. Assert 


### What's in a name?

<!-- .slide: data-background-image="/slides/img/letscode.jpg" data-background-size="contain" data-background-repeat="no-repeat" -->


### Dummy, Stub, Fakes & Mock

- Dummy: Objet par d&eacute;faut.
- Fake: Impl&eacute;mentation limit&eacute;e
- Stub: R&eacute;ponses pr&eacute;d&eacute;dfinies à l'appel de ses m&eacute;thodes
- Mock: Trace le comportement 

Note: 
- Fake: Version appauvrie d'un objet permettant d'ex&eacute;cuter le test (sans framework)
- Stub: Renvoyer la même valeur à chaque appel pour &eacute;liminer un aspect al&eacute;atoire, ou un acc&agrave;s base de donn&eacute;es
- Mock: D&eacute;tecter un &eacute;v&eacute;nement ou un changement d'&eacute;tat au sein d'un objet 


### Confusion

Test Double == Mock ? 
(=Stub/Mock/Fake) 

Note: Il y a confusion sur les objets doublures de test, on les appelle tous Mock... 
Les frameworks participent à cette confusion, car ils m&eacute;langent Stub & Mock al&eacute;grement.


### Soignez vos tests!

Le **code de test** est aussi important que le **code de production** 
Il doit être _aussi propre_ que le code qu'il valide!

Note: Même quand il y a une volont&eacute; de faire des tests, ils peuvent devenir:
- Obsoletes, (&eacute;tat changeant -> tester le comportement et non l'&eacute;tat ?)
- Inmaintenables. (les r&agrave;gles de code propre s'appliquent &eacute;galement au code de test)


### F.I.R.S.T

- Fast
- Isolated
- Repeatable 
- Self-Validating 
- Timely 

Note: 
- Fast => Rapide (car ex&eacute;cuter souvent)
- Isolated => Ind&eacute;pendant (pour ex&eacute;cuter des sous ensembles, ou en parall&agrave;le, ind&eacute;pendemment de l'ordre)
- Repeatable => Admettant d'être rejouer (Sans conserver d'&eacute;tat)
- Self-Validating => Auto-Validant (pas de validation humaine)
- Timely => &eacute;crit avec le code, voir avant (TDD) (En g&eacute;n&eacute;ral, les tests sont meilleurs quand ils sont proche de la conception ou à l'origine du code applicatif). 
https://github.com/ghsukumar/SFDC_Best_Practices/wiki/F.I.R.S.T-Principles-of-Unit-Testing


### Test-Driven Development (TDD)


### Le test comme origine du code

**TODO** <!-- .element: class="fragment highlight-red" data-fragment-index="0"--> 

### Le cycle du TDD

1. Red
2. Green
3. Refactor


### Baby Steps

On favorise toujours les tests et impl&eacute;mentations les plus simples possibles.


### Eloge de la simplicit&eacute;

**TODO** <!-- .element: class="fragment highlight-red" data-fragment-index="0"-->


### R&agrave;gle des 3

Avant 3 occurences, on ne g&eacute;n&eacute;ralise pas un comportement !


### Strat&eacute;gies

- Fake it
- Use Obvious Implementation
- Triangulation ???

Note: 
- Fake it (Doublure temporaire)
- Use Obvious Implementation (Solution &eacute;vidente)
- Triangulation 


## 

<!-- .slide: data-background-image="/slides/img/Fotolia_121049964_M.jpg" data-background-size="contain" data-background-repeat="no-repeat" -->


## R&eacute;f&eacute;rences 

- The Art of Unit Testing, Roy Osherove
- TDD by Example, Kent Beck
- Growing Object-Oriented Software Guided by Tests, Steve Freeman & Nat Pryce 