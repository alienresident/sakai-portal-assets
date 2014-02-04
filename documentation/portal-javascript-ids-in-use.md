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

An alternate list

```
chat.js:57: #pc_connection_chat_" + to + "_messages"
chat.js:70: #pc_editor_for_' + to
chat.js:115: #pc_chat_window_container
chat.js:122: #pc_connection_chat_' + uuid + '_content'
chat.js:143: #pc_editor_for_' + uuid
chat.js:157: #pc_chat_with_' + uuid
chat.js:174: #pc_content
chat.js:175: #pc
chat.js:180: #presenceArea
chat.js:281: #pc_chat_with_" + from
chat.js:288: #pc_connection_chat_' + from + '_content'
chat.js:295: #pc_chat_with_' + from + ' > .pc_connection_chat_title'
chat.js:300: #pc_connection_chat_" + from + "_messages"
chat.js:414: #pc_site_users
chat.js:432: .pc_connection
chat.js:443: .pc_site_user
chat.js:530: #chattableCount
chat.js:576: #pc_pinged_popup_' + userId
chat.js:641: #avatarPermitted
chat.js:660: #pc_connection_chat_" + panelUuid + "_messages"
chat.js:670: #chatToggle
chat.js:723: #pc_connections
chat.js:730: #pc_go_offline_checkbox
chat.js:761: .pc_editor
chat.js:771: #pc_connections_wrapper
chat.js:775: .pc_users_wrapper
chat.js:787: #pc_title
chat.js:795: #pc_showoffline_connections_checkbox
chat.js:801: #pc_users
chat.js:827: #pc_connection_chat_" + sms.uuid + "_messages"
chat.js:867: #footerAppChat

neoscripts.js:404: .more-tab a
neoscripts.js:42: .moreSitesLink
neoscripts.js:313: .nav-selected .icon-sakai-chat
neoscripts.js:418: .nav-selected span: first
neoscripts.js:531: .nav-submenu
neoscripts.js:424: .portletTitle h2
neoscripts.js:342: .toolMenus
neoscripts.js:543: .topnav > li.nav-menu > a
neoscripts.js:474: .trayPopup
neoscripts.js:472: .trayPopupClose
neoscripts.js:60: #allSites
neoscripts.js:269: #container
neoscripts.js:400: #eid
neoscripts.js:353: #maxToolsAnchor
neoscripts.js:573: #maxToolsInt
neoscripts.js:15: #otherSiteList
neoscripts.js:68: #otherSiteList > li:  last
neoscripts.js:18: #otherSitesCategorWrap
neoscripts.js:347: #otherSiteTools
neoscripts.js:375: #otherSiteTools li a:  first
neoscripts.js:266: #portalContainer
neoscripts.js:370: #portalOuterContainer
neoscripts.js:469: #presenceArea
neoscripts.js:310: #presenceCount
neoscripts.js:312: #presenceIframe
neoscripts.js:314: #presenceIframe .presenceList li.inChat span
neoscripts.js:467: #presenceToggle
neoscripts.js:651: #skipNav a.internalSkip
neoscripts.js:494: #subSites
neoscripts.js:628: #toggleNormal
neoscripts.js:256: #toggleNormal em
neoscripts.js:618: #toggler
neoscripts.js:271: #toggleToolMax
neoscripts.js:272: #toggleToolMax em
neoscripts.js:627: #toggleToolMenu
neoscripts.js:52: #txtSearch
neoscripts.js:542:  a.offsite
neoscripts.js:598: ul.subnav
```