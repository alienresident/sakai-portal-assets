## Ids used in `morpheus.scripts.js`
This is a list of IDs used in `morpheus.scripts.js`. To maintain current functionality avoid moving or renaming them without updating the javascript.

Created using this command:
 
```
grep -oh "\w*#\w*" * /portal/portal-charon/charon/src/webapp/scripts/morpheus.scripts.js | sort | uniq
```

List of ids used in `morpheus.scripts.js`:   

```
#allSites
#container
#eid
#imgSearch
#linkNav
#loginLinks
#maxToolsAnchor
#maxToolsInt
#noSearchResults
#otherSiteList
#otherSiteSearch
#otherSiteTools
#otherSitesCategorWrap
#portalContainer
#portalMask
#portalOuterContainer
#presenceArea
#presenceCount
#presenceIframe
#presenceToggle
#selectSite
#skipNav
#subSites
#timeout_alert_body
#toggleNormal
#toggleSubsitesLink
#toggleToolMax
#toggleToolMenu
#toggler
#toolMenuWrap
#txtSearch
```