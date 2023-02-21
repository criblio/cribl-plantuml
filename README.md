# cribl-plantuml

Plantuml Library for Cribl Products

This repository contains an *experimental* library of Plantuml objects for including Cribl products and product components in your plantuml diagrams. 

# Usage

Best practice is to create a "variable" with the URL base, like this:

```
!define criblPuml https://raw.githubusercontent.com/criblio/cribl-plantuml/main
```

You'll also need to include common.puml to get the standard set of components needed:

```
!include criblPuml/common.puml
```

And then finally, include any of the other files:

```
!include criblPuml/product-logos.puml
```

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



### infrastructure-shapes.puml

Sprites and Functions for the Infrastructure Shapes in the Cribl Stencil Set

### knowledge-icons.puml

Sprites and Functions for the Knowledge Icons in the Cribl Stencil Set

### logical_data_flow_shapes.puml

Sprites and Functions for the Logical Data Flow Shapes in the Cribl Stencil Set

