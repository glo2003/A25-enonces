[← Retour](../README.md)

# Tests

## Tests unitaires

Afin d'assurer un bon fonctionnement de chaque partie du code, vous devez tester 
unitairement **toutes les méthodes de toutes vos classes**. Par contre, en pratique, 
on ne teste pas souvent les éléments suivants :

- Les constructeurs (**sauf** pour les validations)
- Les classes de type ressources/contrôleur  (seront testées par intégration/e2e)
- Le "contexte" (`Main`, préparation et enregistrement des resources, etc.)
- Les méthodes de type `get` (sont testées par la bande)

Afin de pouvoir facilement tester des comportements unitaires, vous devrez créer beaucoup 
plus de classes que simplement celles des ressources. Par exemple, pensez à créer des 
*factories* pour la création (avec validations), des classes pour la sauvegarde et la 
recherche/obtention, ou encore des *assembleurs/mappers* pour la conversion logique 
<--> représentaton. Le but est de réussir à tester le plus de comportements possibles!


## Clean code

L'ensemble de vos tests doivent respecter les meilleures pratiques en matière de Clean 
Code. Vous devez donc vous assurer de :

- Avoir un nom représentant clairement les 3 étapes du test (**arrange / act / assert**)
- Avoir un contenu qui représente clairement ces 3 étapes
- Avoir un contenu clair et précis, sans trop de préparation qui viendrait bruiter le test
- Découper le code en sous-fonction et sous-classes lorsque nécessaire
- Préférez l'utilisation de variables pour éviter les *valeurs magiques*

## Changelog

- (27/09/2025): Retrait de la section *Tests d'intégration d'API (Jersey)*.