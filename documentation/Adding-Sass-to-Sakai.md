# Getting Sassy with Sakai

## Summary 
Use [Sass](http://sass-lang.com "Semantically Awesome Style Sheets") to create the new optional responsive skins ([Morpheus](https://jira.sakaiproject.org/browse/SAK-25514 "Jira")) for Sakai 10. Sass enables easier customization and variation without duplicating code and effort. We can do this in such a way that we don't drastically changing the process of creating skins and alienate our current users. 
	
### Advantages of using Sass
* File organization
* DRY and 'Object Oriented' CSS
* Separate presentation styles from layout style for responsive designs
* One codebase: allowing for easier customization and variation
* Create definitive Style Guide and Design Patterns Library

### Proposed workflow
Currently Sakai ships with a large number of example skins (neo-default, neo-default-horiz, neo-default29, neo-examp-u, neo-gen-u, neo-oae, neo-rtl, neo-some-u, neo-ux). The skinning process has been to copy one example skin and start customizing the CSS. i.e. copy `neo-examp-u` to `neo-MY-u`. We want to keep this option available for institutions while switching to Sass for core maintainers.

The proposed workflow is to create a `morpheus-master` folder which will contain the sass scaffolding and a build script (shell script?). The build script will generate and copy the css to the example skins (morpheus-default, morpheus-examp-u, morpheus-rtl). The build script will be run after changes to the sass have been made but before checking in the new CSS to the repo.

The more adventurous skin customizers could take advantage of Sass to customize their skins. There will be documentation on how to do and config files from the example skins. 

As the CSS will be broken down into small discrete files. Maintainers will be able to easily identify what parts of the css they need to update. 

### Example file structures
Example file structure for the skin folder:   

```bash
morpheus-master/  
morpheus-default/
morpheus-examp-u/  
morpheus-rtl/  
```

Example skins' file structure one level deeper: contains only stylesheets and images.

```bash   
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
 
```bash   
morpheus-master/
	config.rb         
	images/
	sass/
	styleguide/
	build-script.sh  // OR pom.xml?      
```   

In the Sass directory there will be a corresponding `scss` file for each compiled `css` file (any `scss` starting with an `_` is consider a 'partial' and is not compiled into it's own css file). 

```bash   
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
		_configurations.scss
		portal.scss
		portal-ie.scss
		styleguide.scss
		tool.scss
		tool-ie.scss
	styleguide/
	build-script.sh       
```

The build script will generate the css for the various example skins. Skin specific values will be control by the `morpheus-master/sass/_configurations.scss` and pull variations from the `morpheus-master/sass/theme` directory.

```bash   
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


  

