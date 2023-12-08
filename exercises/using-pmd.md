# Using PMD

Pick a Java project from Github (see the [instructions](../sujet.md) for suggestions). Run PMD on its source code using any ruleset. Describe below an issue found by PMD that you think should be solved (true positive) and include below the changes you would add to the source code. Describe below an issue found by PMD that is not worth solving (false positive). Explain why you would not solve this issue.

You can use the default [rule base](https://github.com/pmd/pmd/blob/master/pmd-java/src/main/resources/rulesets/java/quickstart.xml) available on the source repository of PMD.

## Answer

En nous servant d ela ligne d'instruction suivante : 
 pmd.bat check -f text -R rulesets/java/quickstart.xml -d [chemin-du-fichier-du-code-source]
Nous exécutons PMD, sur les différents projets java en nous utilisant les différentes rulests .

1- Apache Commons Collections :



