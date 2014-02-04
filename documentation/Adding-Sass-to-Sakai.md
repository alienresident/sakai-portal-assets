# Getting Sassy with Sakai

## Summary 
While we don't want to alienate our current users and drastically change the process of creating skins. 
	
### Goals of using Sass
* Organization
* DRY and 'Object Orientated' CSS
* Ease of customization
* Separate presentation styles from layout for responsive designs
* Create Style Guide and Design Patterns


Example File structure:   

```
morpheus-master/  
morpheus-default/

morpheus-examp-u/  
morpheus-rtl/  
```

Example File structure one level deeper:   

```   
morpheus-default/     
	access.css     
	images/     
	pda.css     
	portal.css      
	portal-ie.css     
	portalchat.css     
	tool.css     
	tool-ie.css   
morpheus-examp-u/   
	access.css   
	images/   
	pda.css   
	portal.css   
	portal-ie.css   
	portalchat.css   
	tool.css   
	tool-ie.css  
morpheus-rtl/   
	access.css   
	images/   
	pda.css   
	portal.css   
	portal-ie.css   
	portalchat.css   
	tool.css   
	tool-ie.css  
```   


```   
morpheus-master/         
	images/
	sass/
	styleguide/
	build-script.sh       
```   

```   
morpheus-master/         
	images/
	sass/
		  _config.scss
		  configs/
		  base/
		  global.scss
		  layout/
		  modules/
		  partials/
		  pattern-primer.scss
		  state/
		  theme/
	styleguide/
	build-script.sh       
```

