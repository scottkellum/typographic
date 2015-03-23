<p align="center">
  <img src="http://corysimmons.github.io/typographic/typographic-logo.svg">
</p>

<p align="center">
  <img src="https://img.shields.io/npm/v/typographic.svg">
  <img src="https://img.shields.io/bower/v/typographic.svg">
  <img src="http://img.shields.io/npm/dm/typographic.svg">
</p>

Typographic is responsive typography made easy. Pick a few font stacks, set a few settings, and you've got **beautiful** responsive typography - it's that easy.


## Installation
- `bower install typographic`
- `@import 'typographic'` somewhere in your Stylus stylesheet


## Usage
It's as easy as setting a few variables in [typographic.styl](typographic.styl] (or letting the defaults do their thing).


## Settings
```stylus
$ratio              = $golden
$body-font          = $helvetica
$body-font-weight   = 300
$body-color         = #666
$header-font        = $helvetica
$header-font-weight = 500
$header-color       = #111
$min-font           = 10px
$max-font           = 16px
$min-width          = 600px
$max-width          = 1000px
```


## Ratios
The ratios are based off of the ratios used on [modular scale](http://www.modularscale.com/).

```stylus
$minor-second   = 1.067
$major-second   = 1.125
$minor-third    = 1.2
$major-third    = 1.25
$perfect-fourth = 1.333
$aug-fourth     = 1.414
$perfect-fifth  = 1.5
$minor-sixth    = 1.6
$golden         = 1.618
$major-sixth    = 1.667
$minor-seventh  = 1.778
$major-seventh  = 1.875
$octave         = 2
$major-tenth    = 2.5
$major-eleventh = 2.667
$major-twelfth  = 3
$double-octave  = 4
```


## Font Stacks
Stacks are picked from A Way Back's [Revised Font Stack](http://www.awayback.com/revised-font-stack/).

```stylus
// Sans-serif

$calibri       = Calibri, Candara, Segoe, "Segoe UI", Optima, Arial, sans-serif
$candara       = Candara, Calibri, Segoe, "Segoe UI", Optima, Arial, sans-serif
$courier       = 'Courier New', Courier, 'Lucida Sans Typewriter', 'Lucida Typewriter', monospace
$franklin      = 'Franklin Gothic Medium', Arial, sans-serif
$futura        = Futura, 'Trebuchet MS', Arial, sans-serif
$geneva        = Geneva, Tahoma, Verdana, sans-serif
$gill-sans     = 'Gill Sans', 'Gill Sans MT', Calibri, sans-serif
$helvetica     = 'Helvetica Neue', Helvetica, Arial, sans-serif
$lucida-grande = 'Lucida Grande', 'Lucida Sans Unicode', 'Lucida Sans', Geneva, Verdana, sans-serif
$optima        = Optima, Segoe, 'Segoe UI', Candara, Calibri, Arial, sans-serif
$segoe         = Segoe, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif
$tahoma        = Tahoma, Geneva, Verdana, sans-serif
$trebuchet     = 'Trebuchet MS', 'Lucida Grande', 'Lucida Sans Unicode', 'Lucida Sans', Tahoma, sans-serif
$verdana       = Verdana, Geneva, sans-serif


// Serif

$antiqua       = 'Book Antiqua', Palatino, 'Palatino Linotype', 'Palatino LT STD', Georgia, serif
$baskerville   = Baskerville, 'Baskerville Old Face', 'Hoefler Text', Garamond, 'Times New Roman', serif
$bodoni        = 'Bodoni MT', Didot, 'Didot LT STD', 'Hoefler Text', Garamond, 'Times New Roman', serif
$cambria       = Cambria, Georgia, serif
$caslon        = 'Big Caslon', 'Book Antiqua', 'Palatino Linotype', Georgia, serif
$constantia    = Constantia, Palatino, 'Palatino Linotype', 'Palatino LT STD', Georgia, serif
$didot         = Didot, 'Didot LT STD', 'Hoefler Text', Garamond, 'Times New Roman', serif
$garamond      = Garamond, Baskerville, 'Baskerville Old Face', 'Hoefler Text', 'Times New Roman', serif
$goudy         = 'Goudy Old Style', Garamond, 'Big Caslon', 'Times New Roman', serif
$hoefler       = 'Hoefler Text', 'Baskerville Old Face', Garamond, 'Times New Roman', serif
$lucida-bright = 'Lucida Bright', Georgia, serif
$palatino      = Palatino, 'Palatino Linotype', 'Palatino LT STD', "Book Antiqua", Georgia, serif
```


## Browser Support
- Full support for IE9+
- IE8 doesn't support [calc](http://caniuse.com/#feat=calc) or [viewport units](http://caniuse.com/#feat=viewport-units) or media queries by default so you shouldn't support it (you will get `$min-font` for all viewport sizes), but if you have a stingy client, you can include these polyfills to at least have it swap between the `$max-font` and `$min-font` at your specified breakpoint.
  - [respond.js](https://github.com/scottjehl/Respond)
  - [calc-polyfill](https://github.com/closingtag/calc-polyfill)
  - [vminpoly](https://github.com/saabi/vminpoly)

### Credit
[Mike Riethmuller](http://twitter.com/MikeRiethmuller) came up with the idea of using `calc` with `vw` to create scaling typography [here](http://madebymike.com.au/writing/precise-control-responsive-typography/).