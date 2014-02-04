# Getting Sassy with Sakai

## Summary 
Use Sass to create the new optional responsive skins (Morpheus) for Sakai 10. Sass enables easier customization and variation without duplicating code and effort. We can do this in such a way that we don't drastically changing the process of creating skins and alienate our current users. 
	
### Advantages of using Sass
* File organization
* DRY and 'Object Orientated' CSS
* Separate presentation styles from layout style for responsive designs
* One codebase: allowing for easy customization and variations
* Create definitive Style Guide and Design Patterns Library

### Proposed workflow
Currently 


### Example file structures
  


Example file structure for the skin folder:   

```
morpheus-master/  
morpheus-default/
morpheus-examp-u/  
morpheus-rtl/  
```

Example skins' file structure one level deeper: contains only stylesheets and images.

```   
morpheus-default/     
	images/         
	portal.css      
	portal-ie.css        
	tool.css     
	tool-ie.css   
morpheus-examp-u/     
	images/    
	portal.css   
	portal-ie.css     
	tool.css   
	tool-ie.css  
morpheus-rtl/   
	images/    
	portal.css   
	portal-ie.css     
	tool.css   
	tool-ie.css  
```   

The big difference is that these example style files will be compiled using a build-script (or perhaps a pom.xml) 
 
```   
morpheus-master/
	config.rb         
	images/
	sass/
	styleguide/
	build-script.sh  // OR pom.xml?      
```   

In the Sass directory there will be a corresponding `scss` file for each compiled `css` file (any `scss` starting with an `_` is consider a 'partial' and is not compiled into it's own css file). 

```   
morpheus-master/
	config.rb            
	images/
	sass/
		base/
		layout/
		modules/
		partials/
		state/
		theme/
		_configs.scss
		portal.scss
		portal-ie.scss
		styleguide.scss
		tool.scss
		tool-ie.scss
	styleguide/
	build-script.sh       
```

The build script will generate the css for the various example skins. Skin specific values will be control by the `morpheus-master/sass/_configs.scss` and pull overrides from the `morpheus-master/sass/theme` directory.


```   
morpheus-master/
	...
	sass/
		...
		theme/
			_morpheus-default.scss
			_morpheus-examp-u.scss  
			_morpheus-rtl.scss	
		_configs.scss
		...  
	...       
```


  

