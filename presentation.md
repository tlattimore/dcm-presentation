---
title: Managing Drupal Configuration Like a Boss
---

# Managing Drupal Configuration Like a Boss
## Thomas Lattimore & Mark Shropshire

---
= data-z="100" data-scale="2"
# So what do we mean by configuration? 

--- 
= data-z="100"
## Storytime…


- You build an awesome site for _UnicornEngine.com_. This includes  some beautifully architected Content Types, polished Views, image style presets, and a lot more that is all glued together by your site building magic.
- The site launches as a huge success and all stakeholders are amazed by your mad skills.


--- 
= data-z="100" data-scale="2"

## But, then they want changes made (of course)
And these changes have to be duplicated across the **test**, **staging**, **demo**, and **live** site for UnicornEngine.

--- 
## So this means I have to point & click across all these sites to make the changes? 
![Picard facepalm](../img/picard-facepalm.gif)

---
## Wrong! [Features](https://drupal.org/project/features) module to the rescue.

___
## Features module allows you to export your site configuration into code that can be deployed to different environments. 
![Picard dance](../img/picard-dancing.gif)

---
An analogy...
![lego - from courtesy of drububu.com](../img/blueprint_lego_bricks.png)

If your Views, content types, taxonomy, and other configuration are "Lego". Features is like storing a blueprint for that configuration *in code*. 

---

## Features history lesson:

- Module name derived from its 1st intent: export "features" for a site. ex: *Blog*, *Photo gallery*, *Store*, etc.
- Geared towards distributions originally. 
- As a side affect it could be used to manage general site configuration.

---

## Features can export:

- Content types & Fields
- Permissions & Roles
- Menus
- {variable} table (with [strongarm](https://drupal.org/project/strongarm) module)
	- This includes site name, slogan, pathauto settings, default theme, and a *lot* more.

---

## Have a need to export something not listed here? There's an API to define your own exportable types.

--- 
## Need more power? We've got modules 

- [Features override](https://drupal.org/project/features_override)
	- If you need to override _existing_ features.
- [Features orphans](https://drupal.org/project/features_orphans)
  - Provides a listing of all configuration that _can_ and _hasn't_ been exported.

___
## Drush integration? Yep, got you covered

- `drush fu {name_of_feature}`
	- update's features with latest configuration in the database
- `drush fr {name_of_feature}` 
	- reverts any configuration in the database that doesn't match what's in a Feature
- See even more examples like creating or editing a Feature from drush in a [High Rock Media blog](http://highrockmedia.com/blog/features-drush-drupal-goodness).

___
## Enough talking - please show me stuff

--- 
## Moving forward...
- Drupal 8 (when it's released) will ship with a configuration management system, built in!
- Features will go back to it's "original" purpose - packaging up "features". Rather than being used also as a universal means of configuration storage
- There is no {variable} table. All configuration is stored in .yml configuration files.

---
## Can I see?

---
## And now, here's shrop!

 



