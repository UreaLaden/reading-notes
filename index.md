# Reading Notes
## Code 301 - Intermediate Software Development
Welcome! This page is a platform for maintaining a record of my **thoughts**, _observations_ and **questions** from reading assignments and discussions throughout the course. 


# Responsive Web Design

Responsive Websites are essentially platform independent. Whether the user is on a mobile phone, tablet or desktop computer, the user experience remains the same. This design is similar, but should not be mistaken for adaptive web design. Adaptive web sites are easily modifiable given specific parameters, while responsive websites continually adjust based on various factors like the size of the view port.The three main components of a responsive web design are flexible layouts, media queries and flexible media. 

## Flexible Layouts

Flexible Layouts consist of grids capable dynamically resizing. These grids use relative length units such as percentages or em units, to declare property values like `width`, `margin`, or `padding`. To maintain flexibility across varying platforms, flexible layouts abstain from using fixed measurement units like pixels or inches. Resizing a column to about 340px can be easily attained using the following formula and block of code.

`target / context = result`

``` css
section {
float:left;
width: 63.197026% ; /* 340px ÷ 538px = .63197026 */
}
```
Derived from [Shay Howes Introduction to Responsive Web Design](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

## Media Queries

Media Queries make it possible to specify specific styles for individual browsers and devices. For example content displayed on a view port with a `width` of 1024px will be different from that of a view port with a `width` of 700px. [Chris Coyier](https://css-tricks.com/css-media-queries/) provides an example of using media queries to determine when specific information and graphics are displayed.

``` css
@media all and (max-width: 699px) and (min-width: 520px){
	#sidebar u li a 
	{
	  padding-left: 21px;
	  background : url(../images/email.png) left center no-repeat;}
	}
```

While the size of the view port is between 520 and 699 pixels, the query uses the extra space to display graphics. Using logical operators like and, not and only, these media queries can be chained together for added effect.

## Flexible Media

Flexible Media is the third major component of responsive design. Similar to flexible grids that adjust in size depending on the size of the view port, images, videos and other types of media need to be constantly adjust as well. This is accomplished using the `max-width` property.

``` css
img, video, canvas
	{
	  max-width: 100%;
	}
```
Derived from [Chris Coyier's CSS Media Queries & Using Available Space](https://css-tricks.com/css-media-queries/)

For this to work effectively, the embedded element must be absolutely position with a parent element that has a `width` of 100%. 

