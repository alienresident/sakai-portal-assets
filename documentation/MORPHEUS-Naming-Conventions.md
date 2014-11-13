# Naming Conventions for MORPHEUS

* [CSS](#CSS-Naming-Conventions-for-MORPHEUS)

## CSS Naming Conventions for MORPHEUS
This is a guide to using naming conventions in the MORPHEUS portal. 

### Why do we need to namespace the portal?
The need for namespacing the portal code has become apparent in the early development of MORPHEUS. We've experienced issues with 3rd party libraries overriding portal css when they share the same name. This is exacerbated when we tried inlining the tools' iFrames. The 3rd party CSS libraries are written in the body of the page and override the portal's CSS in the document head.   

MORPHEUS uses a modified version of [SMACSS](https://smacss.com) (Scalable and Modular Architecture for CSS) as it's categorization methodology. We're using some of the naming  conventions used by [BEM](http://bem.info/method/definitions/) (Block, Element, Modifier) as we found this to be the most scannable method when looking at the source HTML.

### Namespace

CSS must be namespaced using `Mrphs-` which should be written in __PascalCase__.

##### Pattern
```
Mrphs-
``` 

### Modules
Modules are the reusable, modular parts of our design. Modules should be named using __camelCase__.    
This maintains the existing class naming convention in the neo skins and in the underlying Java code. However they should now be prefixed with the `Mrphs-` namespace.


##### Pattern
```
Mrphs-moduleName
```

##### Examples
```
Mrphs-toolNav
Mrphs-button
```


### Module Modifiers
Modifers are changes that extend the base module. Modifiers are suffixed to their modules using two hyphens `--`. Modifiers should be named using __lowercase__.

##### Pattern

```
Mrphs-moduleName--modifer-name
```

##### Examples

```
Mrphs-toolNav--large
Mrphs-button--cancel
```

### Module Elements 

Base modules can have additional elements and they are subclassed using two underscores `__` written in __lowercase__ 

##### Pattern

```
Mrphs-moduleName__element
```

##### Examples

```
Mrphs-searchBox__label
Mrphs-searchBox__input
```

### State Changes

State rules are ways to describe how our modules or layouts will look when in a particular state. Is it hidden or expanded? Is it active or inactive? States are written in __lowercase__ with a single hyphen. They should begin with `is-` and are not namespaced.

##### Pattern

```
is-hidden
```
However states should be chained to their module, modifier, or element. 

##### Examples

```
Mrphs-portalWrapper.is-logged-out
Mrphs-navHeader--small.is-minimized
Mrphs-searchBox__label.is-hidden
```

### Javascript Hooks

Javascript Hooks are ways to indicate that javascript is used to interact with that element. Javascript hooks are written in __lowercase__ with a single hyphen. They should begin with `js-` and are not namespaced. Javascript hooks should be use with other classes for styling and styles should never be assigned to the javascript hook class directly. 

##### Pattern

```
js-action-name
```

##### Examples

```
js-nav-toggle-max
js-nav-toggle-normal
```

## References

* [CSS is a Mess](http://vimeo.com/99877232) – Jonathan Snook – __Beyond Tellerrand__, _Düsseldorf_: 2014 (video)
* [Experimenting with component-based HTML/CSS naming and patterns](https://gist.github.com/necolas/1309546) - Nicolas Gallagher
* [CSS Components, Modifiers, and Subcomponents Collection](https://github.com/bjankord/CSS-Components-Modifiers-And-Subcomponents-Collection) - Brett Jankord
* [SMACSS](https://smacss.com) (Scalable and Modular Architecture for CSS)
* [BEM](http://bem.info/method/definitions/) ( Block, Element, Modifier)
* [Global scope, Namespacing & CSS](https://medium.com/@ahmedelgabri/global-scope-namespacing-css-681bda44c43e) Protecting your CSS from outsiders — Ahmed El Gabri
