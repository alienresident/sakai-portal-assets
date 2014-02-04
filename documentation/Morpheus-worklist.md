# New Optional Responsive Portal
New UI for Sakai CLE (10). A new (responsive) User Interface portal skin initiative is in development. Help contribute ideas, design, and code towards a new style guide  and design pattern library.

## Current Dev Questions

* Dev documentation and assets is now in a [GitHub repo](https://github.com/alienresident/sakai-portal-assets)	
	* Gonzalo's github account?
	 		
* Getting into Trunk Friday 2/7? 
	* Progress? 
	* Best avenue to approach?
* Moving ~~VMs~~ and JS to skin folder
	* Having trouble loading the VMs; It may be the parse functions' relative paths `#parse("/vm/morpheus/includeTabs.vm")`.
	* Here's the Jira [SAK-25456](https://jira.sakaiproject.org/browse/SAK-25456). 
	* It maybe related to the [LibraryWebappLoader.java](http://source.sakaiproject.org/viewsvn/portal/trunk/portal-render-engine-impl/impl/src/java/org/sakaiproject/portal/charon/velocity/LibraryWebappLoader.java?view=markup&pathrev=133274) Need to get John Bush's input. Jira or Email?
	* We should do a merge with portal trunk! That way we can do a merge and bring this in as it'll make testing easier.
	* Should we still move the JS?    
* Adding Sass to Sakai strategies and documentation
	* Will add an outline document.
	
## General Sakai Dev Questions

* Does each tool implement it's own head document or is there a central doc?
*  

## Open Strategic Questions
* __Mobile:__ Help links where do the popup windows go to? Maybe we should add the popup via JS listener rather than hardcoded to the link?
* __Moblie:__ We need a [responsive table](http://css-tricks.com/responsive-data-table-roundup/) strategy.
