# About `theme()`    

+ Declare `library(ggplot2)`.
+ Then, type `? theme` in console will open this document

## Description  

+ A powerful way to customize the non-data components of your plots 
+ i.e. titles, labels, fonts, background, gridlines, and legends. 
+ Allows plots to have a consistent customized look. 

## Theme inheritance  

+ Theme elements inherit properties from other theme elements heirarchically. 
    + For example, `axis.title.x.bottom` inherits from `axis.title.x` which inherits from `axis.title`, which in turn inherits from `text`. 
    + All text elements inherit directly or indirectly from text; 
    + all lines inherit from line, and  
    + all rectangular objects inherit from rect. 
+ This means that you can modify the appearance of multiple elements by setting a single high-level component.

## Arguments  

### Global   

| Category     | Argument                 | Description                                                |    
|:------------:|--------------------------|------------------------------------------------------------| 
|	others	|	...	|	additional element specifications not part of base `ggplot2`. If supplied validateneeds to be set to `FALSE`.	|
|		|	`complete`	|	set this to `TRUE` if this is a complete theme, such as the one returned by `theme_grey()`. Complete themes behave differently when added to a `ggplot` object. Also, when `setting complete = TRUE` all elements will be set to inherit from `blank` elements.	|
|		|	`validate`	|	`TRUE` to run `validate_element()`, `FALSE` to bypass checks.	|
|		|	`line`	|	all `line` elements (`element_line()`)	|
|		|	`rect`	|	all `rect`angular elements (element_rect())	|
|		|	`text`	|	all `text` elements (`element_text()`)	|
|		|	`title`	|	all `title` elements: `plot`, `axes`, `legends` (`element_text()`; inherits from `text`)	|
|		|	`aspect.ratio`	|	aspect ratio of the panel	|

### `panel`  

| Category       | Argument                 | Description                                                |    
|----------------|--------------------------|------------------------------------------------------------| 
|	`panel.spacing`	|	`panel.spacing, panel.spacing.x, panel.spacing.y`	|	spacing between facet panels (unit). `panel.spacing.x` & `panel.spacing.y` inherit from `panel.spacing` or can be specified separately.	|	  
|	`panel.grid`	|	`panel.grid, panel.grid.major, panel.grid.minor, panel.grid.major.x, panel.grid.major.y, panel.grid.minor.x, panel.grid.minor.y`	|	grid lines (`element_line()`). Specify major grid lines, or minor grid lines separately (using `panel.grid.major` or `panel.grid.minor`) or individually for each axis (using `panel.grid.major.x`, `panel.grid.minor.x, panel.grid.major.y, panel.grid.minor.y`). Y axis grid lines are horizontal and x axis grid lines are vertical. `panel.grid.*.*` inherits from `panel.grid.*` which inherits from `panel.grid`, which in turn inherits from `line`	|	  
|	others	|	`panel.background`	|	background of plotting area, drawn underneath plot (`element_rect()`; inherits from `rect`)	|	  
|		|	`panel.border`	|	border around plotting area, drawn on top of plot so that it covers tick marks and grid lines. This should be used with `fill = NA` (`element_rect()`; inherits fromrect)	|	  
|		|	`panel.ontop`	|	option to place the panel (background, gridlines) over the data layers (logical). Usually used with a transparent or blank `panel.background`.	|	  

### `plot`  

| Category     | Argument                 | Description                                                |    
|--------------|--------------------------|------------------------------------------------------------| 
|		|	`plot.background`	|	background of the entire plot (`element_rect()`; inherits from `rect`)	|	  
|		|	`plot.title`	|	plot title (text appearance) (`element_text()`; inherits from `title`) left-aligned by default	|	  
|		|	`plot.subtitle`	|	plot subtitle (text appearance) (`element_text()`; inherits from `title`) left-aligned by default	|	  
|		|	`plot.caption`	|	caption below the plot (text appearance) (`element_text()`; inherits from `title`) right-aligned by default	|	  
|		|	`plot.tag`	|	upper-left label to identify a plot (text appearance) (`element_text()`; inherits from `title`) left-aligned by default	|	   
|		|	`plot.tag.position`	|	The position of the tag as a string (`"topleft", "top", "topright", "left", "right", "bottomleft", "bottom", "bottomright`) or a coordinate. If a string, extra space will be added to accommodate the tag.	|	  
|		|	`plot.margin`	|	margin around entire plot (unit with the sizes of the top, right, bottom, and left margins)	|	  

### `axis`  

| Category     | Argument                 | Description                                                |    
|--------------|--------------------------|------------------------------------------------------------|   
| `axis.title` | `axis.title, axis.title.x, axis.title.y, axis.title.x.top, axis.title.x.bottom, axis.title.y.left, axis.title.y.right`	|	labels of axes (`element_text()`). Specify all axes' labels (`axis.title`), labels by plane (using `axis.title.x` or `axis.title.y`), or individually for each axis (using `axis.title.x.bottom,` `axis.title.x.top`, `axis.title.y.left`, `axis.title.y.right`). `axis.title.*.*` inherits from `axis.title.*` which inherits from `axis.title`, which in turn inherits from `text` |        
| `axis.text`  | `axis.text, axis.text.x, axis.text.y, axis.text.x.top, axis.text.x.bottom, axis.text.y.left, axis.text.y.right`  | tick labels along axes (`element_text()`). Specify all axis tick labels (`axis.text`), tick labels by plane (using `axis.text.x` or `axis.text.y`), or individually for each axis (using `axis.text.x.bottom`, `axis.text.x.top`, `axis.text.y.left`, `axis.text.y.right`). `axis.text.*.*` inherits from `axis.text.*` which inherits from `axis.text`, which in turn inherits from `text` |  
| `axis.ticks` | `axis.ticks, axis.ticks.x, axis.ticks.x.top, axis.ticks.x.bottom, axis.ticks.y, axis.ticks.y.left, axis.ticks.y.right` |	tick marks along axes (`element_line()`). Specify all tick marks (`axis.ticks`), ticks by plane (using `axis.ticks.x` or `axis.ticks.y`), or individually for each axis (using `axis.ticks.x.bottom`, `axis.ticks.x.top`, `axis.ticks.y.left`, `axis.ticks.y.right`). `axis.ticks.*.*` inherits from `axis.ticks.*` which inherits from `axis.ticks`, which in turn inherits from `line` |  
|              | `axis.ticks.length` | length of tick marks (unit) |  
| `axis.line`  | `axis.line, axis.line.x, axis.line.x.top, axis.line.x.bottom, axis.line.y, axis.line.y.left, axis.line.y.right` | lines along axes (`element_line()`). Specify lines along all axes (`axis.line`), lines for each plane (using `axis.line.x` or `axis.line.y`), or individually for each axis (using `axis.line.x.bottom`, `axis.line.x.top`, `axis.line.y.left`, `axis.line.y.right`). `axis.line.*.*` inherits from `axis.line.*` which inherits from `axis.line`, which in turn inherits from `line` |   

### `legend`    

| Category     | Argument                 | Description                                                |    
|--------------|--------------------------|------------------------------------------------------------| 
|	`legend.key`	|	`legend.key`	|	background underneath legend keys (`element_rect()`; inherits from `rect`)	|	  
|		|	`legend.key.size, legend.key.height, legend.key.width`	|	size of legend keys (unit); key background height & width inherit from `legend.key.size` or can be specified separately	|	  
|	`legend.text`	|	`legend.text`	|	legend item labels (`element_text()`; inherits from `text`)	|	  
|		|	`legend.text.align`	|	alignment of legend labels (number from 0 (left) to 1 (right))	|	  
| `legend.title`	|	`legend.title`	|	title of legend (`element_text()`; inherits from `title`)	|	  
|		|	`legend.title.align`	|	alignment of legend title (number from 0 (left) to 1 (right))	|	  
| `legend.box`		|	`legend.box`	|	arrangement of multiple legends (`"horizontal"` or `"vertical"`)	|	  
|		|	`legend.box.just`	|	justification of each legend within the overall bounding box, when there are multiple legends (`"top"`, `"bottom"`, `"left"`, or `"right"`)	|	  
|		|	`legend.box.margin`	|	margins around the full legend area, as specified using `margin()`	|	  
|		|	`legend.box.background`	|	background of legend area (`element_rect()`; inherits from `rect`)	|	  
|		|	`legend.box.spacing`	|	The spacing between the plotting area and the legend box (unit)	|	  
| others |	`legend.background`	|	background of legend (`element_rect()`; inherits from rect)	|	  
|		| `legend.margin`	|	the margin around each legend (`margin()`)	|	  
|		|	`legend.spacing`, `legend.spacing.x`, `legend.spacing.y`	|	the spacing between legends (unit). `legend.spacing.x` & `legend.spacing.y` inherit from `legend.spacing` or can be specified separately	|	    
|		|	`legend.position`	|	the position of legends (`"none", "left", "right", "bottom", "top"`, or two-element numeric vector)	|	  
|		|	`legend.direction`	|	layout of items in legends (`"horizontal"` or `"vertical"`)	|	  
|		|	`legend.justification`	|	anchor point for positioning legend inside plot (`"center"` or two-element numeric vector) or the justification according to the plot area when positioned outside the plot	|	  

### `strip`  

| Category         | Argument                 | Description                                                |    
|------------------|--------------------------|------------------------------------------------------------| 
|	`strip.background`	|	`strip.background, strip.background.x, strip.background.y`	|	background of facet labels (`element_rect()`; inherits from `rect`). Horizontal facet background (`strip.background.x`) & vertical facet background (`strip.background.y`) inherit from strip.background or can be specified separately	|	  
|	`strip.text`	|	`strip.text, strip.text.x, strip.text.y`	|	facet labels (`element_text()`; inherits from `text`). Horizontal facet labels (`strip.text.x`) & vertical facet labels (`strip.text.y`) inherit from `strip.text` or can be specified separately	|	  
|	`strip.switch.pad`	|	`strip.switch.pad.grid`	|	space between strips and axes when strips are switched (unit)	|	  
|		|	`strip.switch.pad.wrap`	|	space between strips and axes when strips are switched (unit)	|	  
|	others	|	`strip.placement`	|	placement of strip with respect to axes, either "inside" or "outside". Only important when axes and strips are on the same side of the plot.	|	  

