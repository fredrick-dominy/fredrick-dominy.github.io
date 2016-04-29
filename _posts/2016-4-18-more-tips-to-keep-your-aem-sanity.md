---
title: Tips to keep your sanity while working with Adobe Experience Manager (AEM)
author: Fredrick Dominy
layout: post
comments: true
tags:
- AEM
- CMS
- tips
---

Following up on my last post of AEM gotchas... This one rang my bell over the weekend when I tried to get a little work done. 

* AEM in editor.html mode won't behave like it should. If you're looking at the functionality of a page make sure to view it as the content alone with ?wcmmode=disabled param.
* Remove the clear icon from Edge with:

```css
    input[type=text]::-ms-clear {  display: none; width : 0; height: 0; }
    input[type=text]::-ms-reveal {  display: none; width : 0; height: 0; }
```

Also, while I was trying to debug some javascript, I found it difficult to work with the minimized and concatenated code in Chrome. A short web search led me to this:

[AEM Configuration Manager](http://localhost:4502/system/console/configMgr)

Once you're there, click on the *Adobe Granite HTML Library Manager* tab and uncheck the Gzip checkbox.