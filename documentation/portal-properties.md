PROPERTIES THAT HAVE AN EFFECT ON PORTAL

```
# whether to pop up tutorial modal on first visit
portal.use.tutorial=false
# wether to show server time on footer
portal.show.time=false 
# wether to show a link to copy the URL of a given tool
portal.tool.direct.url.enabled=true
# Show alternate categorized by term and site type list of "More" sites.
portal.use.dhtml.more=false
# Whether or not to provide a login form on the portal itself (typically on the top). 
top.login=false 
# The URL users are sent to when they click the "logout" button.
loggedOutUrl=
# If you want to send different user types to different URLs when they logout, set this property,
#  eg loggedOutUrl.student=http://someplace.com
# Will fallback to original loggedOutUrl if usertype is not set, or matching property is not set for this user type. 
loggedOutUrl.userType=
# The source location of the login icon displayed in the portal. 
login.icon=
# The textual wording associated with the link to the login URL specified in the login.url property. 
# Will not be displayed on the portal unless top.login is set to false. 
login.text=
# The URL users are sent to when a login is required. This is the destination for the login link as well 
# as the redirect that occurs when a protected resource is accessed without a login. 
login.url=
#The icon associated with the "logout" link. 
logout.icon=
#The textual wording of the link used to log out. 
logout.text=
# Whether or not to show the tool reset button. 
reset.button=
# A URL containing information about this Sakai instance. Can be set to point to a resource stored within Sakai. 
server.info.url=
# The unique identifier for a particular node in a cluster. 
serverId=
# The service hostname for this sakai installation. 
serverName=
# The canonical URL associated with this sakai instance. 
serverUrl=

xlogin.enabled=true/false
xlogin.text=Text to appear
display.users.present=false
portal.experimental.includesubsites=false | never
# A URL that provides accessibility information. The text specified in sit.accessibility is enclosed in the anchor tag associated with this value. 
accessibility.url=
# The text associated with the URL specified in accessibility.url. 
sit.accessibility=
# The copyright text that appears in the footer of the main portal and OSP portal. 
bottom.copyrighttext=
# One or more lines of text (including HTML) that appear as navigational links at the bottom of the main portal and OSP portal. 
bottomnav=
# Whether or not to display the help icon in the upper right of each tool window. 
display.help.icon=
# Whether or not to display a link to help on the left hand navigation menu. 
display.help.menu=
# Whether or not to show the help button. 
help.button=
# A list of tools whose help should not be added to the help index. 
help.hide=
# The tool ID to display when opening the help tool. If specified, the help for the document with this ID will be 
# opened instead of the contextual help for a specific tool 
help.id=
# An external location for help information. 
help.location=
# An external location for help information. 
help.redirect.external.webapp=
# The URL to use instead of the built-in help. 
help.url=

# Whether or not to include subsites in the portal. If set to never, subsites will never be included. 
# If set to false, subsites may be included depending on the site preferences. 
# If set to any other value, subsites will always be included. 
portal.includesubsites=true
# Controls the use of iframes in the PDA portal. If the string contains the text ":none:", 
# then iframes will not be suppressed. If the string contains the text ":all:", then by default 
# all iframes will be suppressed, and only the tools whose ids are specified will be displayed with iframes. 
# If the string contains the text ":debug:", then additional debugging information will be included in the HTML output. 
portal.pda.experimental.iframesuppress=
portal.pda.iframesuppress=
# Whether or not to attempt to generate a custom stylesheet based on the user preferences. 
portal.styleable=
portal.styleable.contentSummary=

# Whether or not to maximize the display when only one site is available. 
portal.experimental.maximizesinglepage=false | true

# The alternate text associated with the image specified in the powered.img property. 
powered.alt=
# The "powered by" image to display in the footer of the main portal and OSP portal. 
powered.img=
# The image specified by the powered.img property will be enclosed in a link to this URL. 
powered.url=
# The text displayed as the root of the bread crumb bar. In other words, the common name of your Sakai instance. 
ui.service=
# The version text that appears next to the word "Sakai" in the footer of the portal. 
version.sakai=
# The version text that appears next to the service name in the footer of the portal. 
version.service=
# default render engine and prefix
# portal.templates=neoskin 
# portal.neoprefix=neo- 

# Tested with a full update from 2-9-x. Here are my test scenarios (I added one) 

# Test 1 - Default settings - no properties 

# Test #2 - Explicit Default Settings 
portal.neoprefix=neo- 
portal.templates=neoskin 

# Test #3 - Old templates, no prefix, old skin (default) 
portal.neoprefix= 
portal.templates=defaultskin 

# Test #4 - New templates, no prefix, old skin (default) (NPE prior to SAK-23395) 
# This will look ugly because it is an old skin (default) with new markup 
portal.neoprefix= 

# Test #5 - New templates, no prefix, new skin (NPE prior to SAK-23395) 
# This will look nice because the new skin (neo-default) matches the new templates 
portal.neoprefix= 
skin.default=neo-default 


# The default skin for sites without a skin setting 
skin.repo=/library/skin  
# Whether or not to allow users to select a custom skin. 
skin.force=
# The relative or absolute URL of the directory containing all available skins. 
skin.root=
# If set to true enables direct urls to access deep content inside a tool.
# Default=true.
charon.directurl=true

# A comma-delimited list of site roles to which users can switch. This allows admins to specify default roles for
#  students if they do not already have a role in the site. 
studentview.roles= 
# My Active Sites drop-down (a.k.a., More Sites)
# Set to true to enable display of the "More Sites" drop-down as a pop-up window organized by site type.
# Default=false;
#portal.use.dhtml.more=true
 
# This setting determines if the portal will reset state at each navigation operation.
#portal.experimental.auto.reset=true
 
# Enable/disable presence display in the portal: always / never / true / false
# If true or false, site presence display may be overwritten by the site property value "display-users-present" (true or false)
# Default=true;
display.users.present=true
 
# Number of tabs to display in the portal before sites are placed into a pulldown menu listing
# Default: 5
#portal.default.tabs=5


# The mobile detection in 2.9 has changed. Tablets are considered regular devices as they have larger screens and are generally more
# capable and given a full screen view.
# Includes iPad, Android (e.g., Xoom), BB Playbook, WebOS, etc.
# The property below is the default
portal.tablets.use.mobile=false

# These two properties control the neochat widget of the portal. By default in 2.9 this is set to false (chat is turned off)
# as this is still an experimental feature which we are testing. We recommend leaving neochat disabled in a
# production environment until performance and usability tests are completed.
portal.neochat=false
portal.neoavatar=true

# Top Dropdown
# These properties control the top dropdown menu. By default they are set to the appropriate tool id.
# If you set them to "none" instead, no link will appear. The last property for portal.use.tutorial is true/false
# and will display or hide the tutorial feature.

#Enable/disable this entire drop down (Set to false to disable)
display.userlogin.info=true
#Enable/disable the showing profile2 link (Set to none to disable)
portal.profiletool=sakai.profile2
#Enable/disable the preferences link (Set to none to disable)
portal.preferencestool=sakai.preferences
#Enable/disable the site setup (Add Tool) link (Set to none to disable)
portal.worksitetool=sakai.sitesetup
#Enable/disable the tutorial tool link (Set to false to disable)
portal.use.tutorial=true

# Help welcome page 
help.welcomepage = /access/content/public/help/index.html
```
NOTES

```
# https://jira.sakaiproject.org/browse/SAK-23224
# Add a wrapper for portal content to allow for good rendering of the JSR-168 Portlet replacement for the web content tool
```


