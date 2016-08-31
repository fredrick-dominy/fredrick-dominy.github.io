---
title: Bind AEM pageProperties to knockout observables
author: Fredrick Dominy
layout: post
comments: true
tags:
- AEM
- CMS
- tips
- knockout
- ko
- observable
- sightly
- HTL
---

We figured out how to introduce AEM pageProperties into the knockout viewModel by a fairly simple instantiation.

First thing was to use sightly expression to send the pageProperty to the knockout observable.

```html
<span class="hide" data-bind="(function() {
    observableVariable( ${ sightlyVariable } );
})()"></span>

```

Usually we instantiate the viewModel with a jQuery $(function() {}); 

Pretty easy...
