# Patrons de création

## Builder (Alias: Monteur)

Permet de construire des objets complexes étape par étape. Il permet de produire différentes variations ou représentations d’un objet en utilisant le même code de construction.

**CAS D'UTILISATION**: Utilisez le patron de conception monteur afin de vous débarrasser d’un « constructeur télescopique ».


## Factory Method (alias: Fabrique)

Définit une interface pour créer des objets dans une classe mère, mais délègue le choix des types d’objets à créer aux sous-classes.

**Possibilité d'application** :  Utilisez la fabrique si vous ne connaissez pas à l’avance les types et dépendances précis des objets que vous allez utiliser dans votre code.

## Prototype (Alias: Clone, Prototype)

Crée de nouveaux objets à partir d’objets existants sans rendre le code dépendant de leur classe.

**CAS D'UTILISATION** : Utilisez le prototype si vous ne voulez pas que votre code dépende des classes concrètes des objets que vous clonez.


## Singleton

Garantit à l'instance d'une classe qu'elle existe en un seul exemplaire. Elle fournit un point d'accès global à cette unique instance.

**CAS D'UTILISATION**: Utilisez le singleton lorsque l’une de vos classes ne doit fournir qu’une seule instance à tous ses clients. Par exemple, une base
de données partagée entre toutes les parties d’un programme. Utilisez le singleton lorsque vous voulez un contrôle absolu
sur vos variables globales.





