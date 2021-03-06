# Getting Sassy with Sakai

## Summary 
Use [Sass](http://sass-lang.com "Semantically Awesome Style Sheets") to create the new optional responsive skins ([Morpheus](https://jira.sakaiproject.org/browse/SAK-25514 "Jira")) for Sakai 10. Sass enables easier customization and variation without duplicating code and effort. We can do this in such a way that we don't drastically changing the process of creating skins and alienate our current users. 
	
### Advantages of using Sass
* File organization
* DRY and 'Object Oriented' CSS
* Separate presentation styles from layout style for responsive designs
* One codebase: allowing for easier customization and variation
* Create definitive Style Guide and Design Patterns Library

### Current workflow
Currently Sakai ships with a large number of example skins (neo-default, neo-default-horiz, neo-default29, neo-examp-u, neo-gen-u, neo-oae, neo-rtl, neo-some-u, neo-ux). The skinning process has been to copy one example skin and start customizing the CSS. i.e. copy `neo-examp-u` to `neo-MY-u`. We want to keep this option available for institutions while switching to Sass for core maintainers.

#### Issue of introducing Sass into the current workflow
Sass is a CSS preprocessor so any edits directly on the CSS files will be overwritten the next time the Sass compiled. Edits need to be added directly to the SCSS files instead. The barrier to entry is low as SCSS is a superset of CSS and vanilla CSS will work. The only issue is to make sure that developers understand the modified workflow.  

### Proposed workflow
The proposed workflow is to create a `morpheus-master` folder which will contain the sass scaffolding and a compile script (ruby script). The compile script will generate and copy the css to the example skins (morpheus-default, morpheus-examp-u, morpheus-rtl). The compile script will be run after changes to the sass have been made but _before_ checking in the new CSS to the repo.

The more adventurous skin customizers could take advantage of Sass to customize their skins. There will be documentation on how to do and config files from the example skins. 

As the CSS will be broken down into small discrete files. Maintainers will be able to easily identify what parts of the css they need to update. 

#### Sakai 11 workflow
If morpheus becomes the default skin in Sakai 11 it then makes sense to use the [sass maven plugin](https://github.com/Jasig/sass-maven-plugin) to preprocess the Sass into CSS. If this is configurable to only be used if morpheus is selected then it would be good to add it for Sakai 10.

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

The big difference is that these example style files will be compiled using `Sakai-Compass-Compile.rb`
 
```   
morpheus-master/
	config.rb         
	images/
	sass/
	styleguide/
	Sakai-Compass-Compile.rb     
```   

In the Sass directory there will be a corresponding `.scss` file for each processed `.css` file. __Note:__ any `scss` beginning with a `_` is consider a 'partial' and is not processed into a corresponding CSS file. 

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
		_configurations.scss
		portal.scss
		portal-ie.scss
		styleguide.scss
		tool.scss
		tool-ie.scss
	styleguide/
	Sakai-Compass-Compile.rb
```

The compile script will be used to generate the css for the various example skins. Skin specific values will be controlled in the `morpheus-master/sass/_configurations.scss` and this will pull in variations from the `morpheus-master/sass/theme` directory.

```   
morpheus-master/
	...
	sass/
		...
		theme/
			_morpheus-default.scss
			_morpheus-examp-u.scss  
			_morpheus-rtl.scss	
		_configurations.scss
		...  
	...       
```