---
layout: article
permalink: /
title: "BMJ FEF Prototyper"
excerpt: "A Rapid Prototyping Framework"
modified: 2015-03-4
image: 
  feature: generic-feature.jpg
  teaser: generic-teaser.jpg 
  thumb:  generic-thumb.jpg
category: articles
tags: [rapid prototyping, jekyll, web development, design, open source]
comments: true
id: home
ads: false
share: false
sidebar: sidebar-home
---

The idea here is to create a forkable FE framework, specifically for rapid protoyping ... new features, new sites - you name it. But first a few caveats! Nice people on GitHub like to offer up they're hard work for the benefit of people with different or lesser skills. Being a mere designer, I've taken advantage of that to some extent here and will credit those people in due course (i.e. very soon when I know who needs the attribution!).

It has bothered me for sometime (I'm like that!) that we don't have a site-wide BMJ 'theme' that we can turn to when we are asked to mock something up. Now that we are becoming more UX-aware, we like to get 'stuff' in front of users on occassion and I hope this framework will serve that purpose well.

Eventually (I hope!) the 'stuff' prototyped with this framework will be handed over to our dev's with minimal fuss (zero hand-over friction!) and production-ready code. It may take a few iterations but thats the overarching goal. I know the devs are working on their side to a similar end and maybe we'll meet in the middle.

{% include toc.html %}

## An introduction

I’ve used a few tools over the years and, while I’m not out to find the very best of the best (not sure I'd recognise it!), there are some criteria for success. IMO a good prototyping tool should:

*  have a gentle learning curve, but hidden extras that can be introduced over time.
*  be able to accommodate site-wide changes readily, without the need to rebuild structure or duplicate work.
*  be able to move seamlessly from prototype to production (so we can really advance the prototype before Sprint No1 starts)
*  offer an easy way of extending or adding more complex (javascript?) functionality like modals, carousels (yuck!) etc.
*  kinda step aside so designers can think about the design - the UI, UX - and not the implementation.

The framework also includes a [styleguide](http://localhost:4000/style-guide/) which can be customised as necessary and sit under our core 'living stylguide' for new products or features. This was a happy byproduct of customising this framework. It offered the opportunity to work from the ground up and re-examine our current online styleguide. More on that later... 

### Another reason...

Another reason for wanting to explore the possibilities of a prototyping framework is control. Designers are control freaks (aka disgruntled observationalists) and taming design in such a large organisation is a Sisyphean task. The ultimate with this is that our core products begin to align in terms of the user interface, experience and engagement.

## What's this about then?

The main stars of the framework are Jekyll and Liquid. However I’ll also point out some of the supporting cast, as well as why I picked them.

### Jekyll

[Jekyll](http://jekyllrb.com/) is the static-site generator of choice --- it seems to meet the criteria above. The same can be said for [Liquid](http://liquidmarkup.org/) which (till now at least) has supported every template layout required.

Publishing a new post - pages later - as follows:

1.	Create a text file written in Markdown for a new post (templates are used to lay these out).
2.	Add a <abbr>YAML</abbr> Front Matter block to the top of these files to indicate which layout to use, the post's meta data, feature image, category, and tags.
3.	Run `jekyll` from the <abbr title="Command line">CLI</abbr> to spit out the compiled site.
4.	Deploy `/_site` to my web server using a rake task that minifies all .html files, rsyncs the changes, and pings Google and Bing notifying them that `sitemap.xml` has updated.

There can be a few more steps to the process, but for the most part it's fairly straight forward after you've built all the necessary `_layouts` and `_includes`. 

Jekyll allows you to familiarise yourself with the basics of HTML5 and CSS3 transitions (some evident here), be able to design every page without hacks, get nice with CSS preprocessors like [Sass](http://sass-lang.com/) to create more powerful and efficient stylesheets, and design responsively.

### Compass SASS and Vertical Rhythm

Details of vertical rhythm for typograhy .... along with company move to sass. Controversial choice of not including thrird party framework (Bootstrap , Foundation etc) but custom components. Also...

### A Grid System?

Using Neat (a lightweight semantic grid framework for Sass and Bourbon), is an easy way to establish a grid system in the layouts, and allows us to dicth the semantically unfriendly practice of using classes like `.grid_x`, `.push_x`, or `col_x`. Elsewhere in the tech dept, however, Susy seems to be the grid system of choice so I'll revisit this section and update.

<div class="notice-warning" markdown="1">
#### Using Bourbon & Neat for the grid system (& moving to Susy)
[Bourbon](http://bourbon.io) and [Neat](http://neat.bourbon.io/) to manage my mixins and grid. [Susy](http://susy.oddbird.net/) looks like something we all want to move to (why?), so I'll swap with Neat once I have the time to play around with it.
</div>

## What's Left to Do? (lots but need to get my head around this!)

1.	Bring it fully inline with our brand
2.	Introduce Susy to replce Neat grid system
3.	Trial it with designers & devs for feedback
4.	Finalise the styleguide (this might inform our core style? Typography definitely...)
5.	Create additional templates (discuss with designers / feds)
5.	Learn how to utilise rsync and rake tasks to simplify deployment


### Version Control

There will be a soon-to-be-released 1.0, once some of the above is dealt with. There is a [repository on GitHub](https://github.com/moconnor-bmj/BMJ-FEF). Should we demand version controlling each update? 

It would be wise to learn how to utilise rsync and rake tasks to make deploying easier instead of manually FTPing the contents of `_site\` to the server.

<div class="notice-info" markdown="1">
#### This is a work in progress & contributions wanted!
The [sourcecode for this BMJ-FEF](https://github.com/moconnor-bmj/BMJ-FEF) is on GitHub if you want it. Feel free to fork the repo and contribute....
</div>