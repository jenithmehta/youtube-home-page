### Title: HTML & CSS Notes

> > NOTE: If struggling with some css implementation, try to implement it in a new html on a small scale

> Q. What are void elements in html?

- Elements that do not require closing tags are called void elements, example. link, br

`NOTE: use https://fonts.google.com for fonts`

> Q. what is object-fit?

- this is a property that lets us decide how should the image fit.
- if it is set to 'cover'. then the image will fit the desired size but not grow beyond it. this will not strech or squeeze the image.
- 'contain' - this will minimize the image to fit a particular size. this will always display the full image and not crop it.

> Q. what is flex attribute, how to use it

- flex is align elements column wise or row wise
- flex also provides auto zoom and shrink capabilities
- flex consists of 3 properties
- flex-grow: how many multiple the element should grow on zooming in compared to other elements
- flex-shrink: opposite of flex-grow
- flex-basis: initial size of the element. it is either auto or set in pixels.
- value 0 means no effect on zooming in/out. it means the element is not flexible

> explain display: flex

- flex gives alignment capabilities
- there are 2 axis, main axis and one that runs perpendicular to it.
- main axis is represented by flex-direction property
- other one cross-axis
- flex-direction can take 4 values
  - row, row-reverse, column and column-reverse
  - row will align along the x-axis
  - whereas column will align the elements along the y-axis
  - we have reverse options because flex does not want to assume the direction of the next element
- area under flex-box is called flex-container
- once a div is set to flex, then its child items automatically become flex-items
- flex: 1, this is equivalent to 1fr of grid. Basically div takes the rest of available space
- justify-content: this property helps in aligning flex items in the direction of flex. for row flex, it aligns items horizontally.

  - center, aligns them at center
  - start,end are other options
  - space-between aligns to spread across the container equally

- align-items: this property is useful for cross-axis alignment. for row flex it aligns items vertically ( this is a flex property, for grid, align-content may work)
  - strech: default property, vertically takes up the whole space
  - start: takes up only required space from top
  - end: reverse of start
  - center: aligns vertically to center
    > > Note: for alignining there are two types, items & content. distinction is not clear at moment, but both can be tried, one should work. If it does not work then check if the items in container have fixed height and width.

> Q. Why does my search bar and search button have different hieght when their values are same?

- Not important, should continue with video

> Q. what is font weight?

- It is how thick and dark a text should appear

> Q. what is block element?

- It takes up the whole line
- eg. the paragraph element
- block element can be converted to inline block `display: inline-block`
- block element takes whole line of its container. If it is in a div element, it will occupy the width of the div element.

> Q. what is an inline block element

- It does not take up the entire line
- eg. image element, input element

> Q. what is an inline element?

- an element within in a line of text

> how to align elements?

- property | vertical-align: top;
- this propertly aligns the element to the top
- when the same class is used by different containers, all can be aligned to the top

> what is nested layouts technique?

- A design is divided into vertical and horizontal elements. The design can be constructed using block and inline div elements.
- eg. design breakdown of one the video preview
  ![alt text](../misc/layout-example.png)
- Note: divs by default take up 100% width so they do not appear side by side even when selected display: inline-block. In such cases, need to reduce the width to accomodate both the divs
- images by default overflow div. For this create a class for image and set it to 100%. So the image would occupy the 100% width of its container i.e. div

> Grids have much better alignment than inline blocks

- display: grid;
- grid-template-columns: 100px 100px;
  this will create 2 columns each of 100px
- grid-template-columns: 100px 1fr;
  fr stands for free space
  this will create 2 columns, one of 100px and second column of the remaining width available in the container.
