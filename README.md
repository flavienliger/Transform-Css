Transform-Css
=============

Convert transform to Js, get current transform for translate/scale/rotate.

Notice
======

Input avalaible :
- string Css 'translateX(90px)'
- object { translateX: 90 }
- jQuery Object $el

/!\ Warning /!\ for the state before, you shouldn't use Css style sheet, use $.css or el.style for set transform.