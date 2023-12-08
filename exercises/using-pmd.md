# Using PMD

Pick a Java project from Github (see the [instructions](../sujet.md) for suggestions). Run PMD on its source code using any ruleset. Describe below an issue found by PMD that you think should be solved (true positive) and include below the changes you would add to the source code. Describe below an issue found by PMD that is not worth solving (false positive). Explain why you would not solve this issue.

You can use the default [rule base](https://github.com/pmd/pmd/blob/master/pmd-java/src/main/resources/rulesets/java/quickstart.xml) available on the source repository of PMD.

## Answer

En nous servant d ela ligne d'instruction suivante : 
 pmd.bat check -f text -R rulesets/java/quickstart.xml -d [chemin-du-fichier-du-code-source]
Nous exécutons PMD, sur les différents projets java en nous utilisant les différentes rulests .

1- Apache Commons Collections :

Les faux-positifs :

° This if statement can be replaced by `return !{condition} && {thenBranch};` : 
Il s'agit dans ce cas de la structure du code. En gros PMD estime que le code pourrait être réduit en utilisant un return au lieu d'utiliser les conditions if. Il est question ici d'un faux-positif, parce qu'en effet dans le code les valeurs retournées dans les conditions ne sont pas des booléens, mais aussi il y a une levée d'exception.
*commons-collections-master\commons-collections-master\src\main\java\org\apache\commons\collections4\bloomfilter\IndexFilter.java*  _ligne 75_

° Avoid assignments in operands : 
Cette règle a pour but de faciliter la lecture du code. Elle conciste à évitér toutes assignation (initialisation) de variables dans les opérandes des conditions. Dans notre cas il s'agit d'un faux positif selon nous parce que l'assignations éffectuées dans la condition if, ne rend pas plus compliqué le code à la lecture.
*commons-collections-master\commons-collections-master\src\main\java\org\apache\commons\collections4\bloomfilter\ArrayCountingBloomFilter.java*  _ligne 198_

Les vrai-positifs :



