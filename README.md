colors
=========

This package contains a list of colors in image.color GGBA format.
The first set of colors is the colors specified by the HTML 4 standard.
The second set of  colors are the colors specified by the CSS3 standard as described in http://www.w3.org/TR/css3-color/#svg-color .

This package is go gettable, so one can download the package with the command: 
`go get github.com/btracey/colors` . 
If one is going to use a lot of the colors in a code, the package may be imported with an alias to allow easier typing. For example, `import cl "github.com/btracey/colors"`
and then one can use cl.Black instead of colors.Black

All of the colors are variable declarations. If one wants to have multiple independent pointers to this variable, it is necessary to create a new structure first before referencing it. For example

	p1 := &colors.Black //Creates a pointer to the colors.Black variable
	p2 := &colors.Black //Creates another pointer to the colors.Black variable
	v1 := colors.Black //Creates a copy of the colors.Black variable
	p3 := &v1 //Creates a pointer to the copy

If p1 is modified, p2 will be modified as well, whereas p3 will not, because it is a reference to the copy, rather than to the package variable.  
