# Getting Sassy with Sakai

## Summary 
While we don't want to alienate our current users and drastically change the process of creating skins. 
	
### Goals of using Sass
* Organization
* DRY and 'Object Orientated' CSS
* Ease of customization
* Separate presentation styles from layout for responsive designs
* Create Style Guide and Design Patterns


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


  

