# IMPORTANT

## Ce fichier est une archive expliquant le choix de passer en Monorepo

## Il n'est donc pas à jour mais est volontairement laissé comme tel afin de démontrer les recherches pour effectuer ce choix

--------

# Architecture actuelle (Subrepos)

### Avantages

> Division du code dans les repos pertinents

### Inconvénients

> Process trop complexe

- 4 Repos à gérer

	- NoLoBack
		- NoLoAPI
			- NoLoNestModules
		- NoLoVideo
			- NoLoNestModules (même que précédent)

	- Versioning compliqué
		- Problèmes liés au repo partagé (ex: désync, prisma...)

	- Très lourd à gérer 

------

# Architecture future (Monorepo)

### Avantages

> Process Simple

- Pas de désync des sous modules (ex: NoLoNestModules)
- Un seul versioning pour chaque app

- Nx
	- Fournit une suite d'outil de productivité
	- Prévient automatiquement en cas de breaking change sur une dépendance
	- Nx Cloud

![[nx.png]]

### Inconvénients

> Code complètement centralisé en un repo : Peut devenir très lourd

##### Arbre de dépendances back après migration monorepo

![[app-graph.png]]
> Arbre généré automatiquement par Nx
