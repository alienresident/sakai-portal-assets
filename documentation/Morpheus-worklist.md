# MORPHEUS
Mobile Optimized Responsive Portal for Higher Education Using Sass

New UI for Sakai CLE (10). A new (responsive) User Interface portal skin initiative is in development. Help contribute ideas, design, and code towards a new style guide  and design pattern library.

## Current Dev Questions

* Dev documentation and assets is now in a [GitHub repo](https://github.com/alienresident/sakai-portal-assets)	
	* Gonzalo's github account: [gsilver](https://github.com/gsilver)
	 		
* ~~Getting into Trunk Friday 2/7?~~ DONE!!
   
* Moving VMs to skin folder
	* Having trouble loading the VMs; It may be the parse functions' relative paths `#parse("/vm/morpheus/includeTabs.vm")`.
	* Here's the Jira [SAK-25456](https://jira.sakaiproject.org/browse/SAK-25456). 
	* It maybe related to the [LibraryWebappLoader.java](http://source.sakaiproject.org/viewsvn/portal/trunk/portal-render-engine-impl/impl/src/java/org/sakaiproject/portal/charon/velocity/LibraryWebappLoader.java?view=markup&pathrev=133274) Need to get John Bush's input. Jira or Email?
	* ~~We should do a merge with portal trunk! That way we can do a merge and bring this in as it'll make testing easier.~~ DONE
	
* Moving JS to skin folder
	* ~~Should we still move the JS?~~ YES   
	* Are there other JS files we should move? MAYBE
	
* Adding Sass to Sakai strategies and documentation
	* ~~Will add an~~ [Outline Document](https://github.com/alienresident/sakai-portal-assets/blob/master/documentation/Adding-Sass-to-Sakai.md)   
	
## General Sakai Dev Questions

* Does each tool implement it's own head document or is there a central area?  
 
Is this a list of all the files to do with creating a header for tools?

``` 
./login/login-authn-tool/tool/src/java/org/sakaiproject/login/tool/AuthnPortal.java
./portal/portal-impl/impl/src/java/org/sakaiproject/portal/charon/CharonPortal.java
./portal/portal-impl/impl/src/java/org/sakaiproject/portal/charon/SkinnableCharonPortal.java
./portal/portal-render-engine-impl/impl/src/java/org/sakaiproject/portal/charon/velocity/VelocityPortalRenderEngine.java
./portal/portal-render-engine-impl/pack/src/test/org/sakaiproject/portal/charon/test/MockCharonPortal.java
./portal/portal-tool/tool/src/java/org/sakaiproject/portal/tool/ToolPortal.java
``` 
  

## Open Mobile Strategy Questions
* __Mobile:__ Help links where do the popup windows go to? Maybe we should add the popup via JS listener rather than hardcoded to the link?
* __Moblie:__ We need a [responsive table](http://css-tricks.com/responsive-data-table-roundup/) strategy.

## UMich worklist

### Portal work that needs to be done
* Menus Responsive positioning (M)
* Icon font (M)
* ~~Build Script (M|NYU) ~~
* Footer (G)
* Javascript: To optionally set the drop down on the site menus (G)

### Tool work 
* Markup for Tool Nav (G)
* Tool head add IE stylesheets (G will investigate)
* Add tool.id class to body tag (G will investigate)
* HTML 5 and ARIA are we covering the basics?
* Role Switcher to drop down from Select Menu (G)
* Morpheus language bundle can we change things independently from Neo


## Open Apereo worklist

### Road Map: What's next?

1. Finish adding modules from NYU Classes code base
2. Responsive menus for devices
3. Responsive typography
4. Flesh out examples skins
5. User Testing
6. Documentation

### To dos
* Add [color contrast mixin](https://github.com/voxpelli/sass-color-helpers) to report WCAG contrast issues


