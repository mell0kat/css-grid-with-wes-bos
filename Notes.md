display: grid makes all direct children

grid gap is like margin bettween tracks

see 04- Line Meanings diagram to see what all of the dotted + dashed lines mean

### Implicit vs. explicit grids
implicit - if you do not define them

e.g. you say grid-template-columns: 200px 400px;
but do not define rows, it will wrap as necessary
dotted-implicit grids
dashed - exlpicit rows

grid-auto-rows for any extra implicitly created rows


### CSS-grid-auto-flow
defines where new items are placed if there are more items than explicitly defined grids
by default, extra items are placed into a new row

### Sizing tracks in CSS grid
percentages not advised because it can cause horizontal scroll due to grid gap

use the FR unit (fractionl) - represent teh mount of the space left over after all items are laid out

default height of element - height of content

default width - width of viewport

auto keyword - elements sized to the widest content

### CSS Grid Repeat Function
shorthand
grid-template-columns: 1fr 1fr 1fr 1fr;

becomes
grid-template-columns: repeat(4, 1fr)

### Sizing grid items
Use grid-column: span 2; and/ or
grid-row: span 2; to tell your grid item to take up more space

this is a better alternative that explicitly setting width

grid-column is actually shorthand for
grid-column-start: span 2;
grid-column-end: auto;

### Placing Grid items
either use track numbers or use 'span value' to say how long it is

grid-column: start (# or span #) / end (# or span #)

can use negative numbers

### Autofill and Autofit
* auto-fill adds columns / rows as appropriate to fill the grid
* diff. b/w the two only evident when few items
  * autofill cuts off grid at full width
  * auto-fit cuts off grid at end of items

### Minmax() for responsive grids
* autofit in combination with minmax() deliver a reponsive grid
` grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));`

### Grid template areas
* Use grid-template-areas on container to name your sections
* Use grid-area to assign your grid items to take up specified space
* Can use area-names to specify start / end of columns and rows
```
		.container {
      grid-template-areas:
      "P P P P H H H H"
      "P P P P H H H H"
      "P P P P H H H H"
      "P P P P H H H H"
    }

    .item3 {
      grid-column: P-start / P-end
    }
```

### Naming lines
* Use square brackets when defining columns and rows
```
 grid-template-columns: [site-left] 1fr [content-start] 500px [contane-end] 1fr [site-right];
 ```

### Grid auto-flow dense
* shifts items around to pack in as many with as little empty space
* CSS will always layout the items that are more specific (e.g. grid-column-end: -1) first, and then do autoflow for the rest

### Grid alignment and centering
* what's available:
	* justify-items
	* align-items
	* justify-content
	* align-content (these two used for dealing with space between / around items if you have extra space)
	* justify-self
	* align-self
* values can be:
  * start
  * end
  * stretch
  * center
* place-items is a shorthand combination of justify-items and align-items

* justify along row axis
* align along column axis

### Nesting grids
* is possible

### Image Gallery
* Can overlay items by placing them in the same row & column and then use z- index as needed
* #rrggbbaa (who knew??)
