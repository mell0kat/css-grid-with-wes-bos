![](https://res.cloudinary.com/wesbos/image/upload/v1515524452/GRID-social-share_wlfzk3.png)

# CSS Grid Video Course

I'm taking Wes Bos's CSS Grid Course, which I found over at [CSSGrid.io](https://CSSGrid.io).

## My Notes

### Foundations
* display: grid makes all direct children
* `grid-gap` is like margin between tracks
* see 04- Line Meanings diagram to see what all of the dotted + dashed lines mean

### Implicit vs. explicit grids
* implicit - if you do not define them

e.g. you say grid-template-columns: 200px 400px;
but do not define rows, it will wrap as necessary
dotted - implicit grids
dashed - explicit rows

* grid-auto-rows for any extra implicitly created rows


### CSS-grid-auto-flow
* defines where new items are placed if there are more items than explicitly defined grids
by default, extra items are placed into a new row

### Sizing tracks in CSS grid
* percentages not advised because it can cause horizontal scroll due to grid gap
* use the FR unit (fractionl) - represent teh mount of the space left over after all items are laid out
* default height of element - height of content
* default width - width of viewport
* auto keyword - elements sized to the widest content

### CSS Grid Repeat Function
shorthand
`grid-template-columns: 1fr 1fr 1fr 1fr;`
becomes
`grid-template-columns: repeat(4, 1fr)`

### Sizing grid items
Use grid-column: span 2; and/ or
grid-row: span 2; to tell your grid item to take up more space

this is a better alternative that explicitly setting width

grid-column is actually shorthand for
grid-column-start: span 2;
grid-column-end: auto;

### Placing Grid items
* either use track numbers or use 'span value' to say how long it is
`grid-column: start (# or span #) / end (# or span #)`
*can use negative numbers

### Autofill and Autofit
* auto-fill adds columns / rows as appropriate to fill the grid
* diff. b/w the two only evident when few items
  * autofill cuts off grid at full width
  * auto-fit cuts off grid at end of items

### Minmax() for responsive grids
* autofit in combination with minmax() deliver a reponsive grid
` grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));`




