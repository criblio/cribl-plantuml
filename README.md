# cribl-plantuml

Plantuml Library for Cribl Products

This repository contains an *experimental* library of Plantuml objects for including Cribl products and product components in your plantuml diagrams. 

# Files

### common.puml 
sets up a few common items that will be used by the other files. 

### activity-badges.puml
A convenience library of numbered meatballs for showing order of operation in non-activity diagrams. 

### product-logos.puml
Sprites and "Functions" for each of the Cribl Products:

* Stream (CriblStream)
* Edge (CriblEdge)
* Search (CriblSearch)

Each "function" can be use with the following argument structure:

```
Function(<id>, <label>, <shape>, <color>)
```

The only required option is id, and the other positional arguments default to:

* \<label> - blank
* \<shape> - rectangle
* \<color> - Cribl Aqua

for example: 
```
@startuml
!define criblPuml https://raw.githubusercontent.com/criblio/cribl-plantuml/main
!include criblPuml/common.puml
!include criblPuml/product-logos.puml

CriblSearch(search, "Search Instance", cloud, blue)
@enduml
```

will generate the following:
![Cribl Search Image](images/search-example.png)