# Tricks
## Fix <a> tag being bigger than its content
I realized while trying to create a menu using SVG elements inside an `a` tag
that this had a bit more of height that the svg. It turned out that to fix it
I had to set the content of `<a>` to `display: flex`.

##  Center an image in the line:
```css
 IMG.displayed {
    display: block;
    margin-left: auto;
    margin-right: auto }
```

[source](https://www.w3.org/Style/Examples/007/center.en.html)

## Make any DOM element to propagate focus and blur event
When you have a DOM element that doesn't propagates the focus and blur events and
you want it to do so, you can add to it the tabindex attribute (with a tabindex of -1 will do the trick)

## Center an object exactly in the middle of the screen:
```css
.center {
     position: fixed;
     left: 50%;
     top: 50%;
     transform: translate(-50%, -50%);
 }
 ```
 [explanation post](https://css-tricks.com/quick-css-trick-how-to-center-an-object-exactly-in-the-center/)

## Box Shadow css trick
[article](https://css-tricks.com/snippets/css/css-box-shadow/)

## Col same size with bootstrap
Add this class to you css
```
.row-eq-height {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display:         flex;

}

```
[source](http://getbootstrap.com.vn/examples/equal-height-columns/)

## Position element in the lower right corner
```
.box {
    position:relative;

}
.bet_time {
    position:absolute;
    bottom:0;
    right:0;

}
```
> The way this works is that absolutely positioned elements are always positioned with respect to the first relatively positioned parent element, or the window. Because we set the box's position to relative, .bet_time positions its right edge to the right edge of .box and its bottom edge to the bottom edge of .box

[source](http://stackoverflow.com/questions/3956043/css-how-to-position-element-in-lower-right)

## Sticky footer
How to kept the footer at the bottom even though your content doesn't fill the
whole height of the display

[source](https://philipwalton.github.io/solved-by-flexbox/demos/sticky-footer/)

* An alternative with just css [Sticky footer - CSS tricks](https://css-tricks.com/snippets/css/sticky-footer/)
```html
<body>
    <header></header>
    <article></article>
    <footer></footer>
</body>
```

```css
body {
    height:100%;
}

header {
    height: 50px;
}

footer{
    height: 50px;
}

article{
    height:100%;
   /* The header and footer height respectively */ 
    margin-bottom: -50px;
    margin-top: -50px;
}
```

> This is a really simple implementation. Do not style your web by 
targeting tags with your css :P

##Align form elements
```
    <form class="user-form">
        <div class="field">
            <label for="firstname">First Name:</label>
            <input name="firstname" type="text" size="50" autofocus />
        </div>
        <div class="field">
            <label for="lastname">Last Name:</label>
            <input type="text" name="lastname" size="50" />
        </div>
        <div class="field">
            <label for="birthdate">Birth Date:</label>
            <input type="date" name="bdate" size="50" />
        </div>
    <form>
```

```
    .user-form { padding:20px;  }

    .user-form .field { padding: 4px; margin:1px; background: #eee;  }

    .user-form .field label { display:inline-block; width:120px; margin-left:5px;  }

    .user-form .field input { display:inline-block;  }
```

[Aligning HTML5 form elements](http://stackoverflow.com/questions/17825979/aligning-html5-form-elements)

## Div element size doesn't increase if it has floated elements
[StackOverflow ask](http://stackoverflow.com/questions/16568272/why-doesnt-the-height-of-a-container-element-increase-if-it-contains-floated-el)

The solution is adding a `clear: both;` div after the div with floated elements

## Importance rules

The CSS importance is at follows

> attributes < stylesheet < inline css

## Select All elements but it's last child

```css
p:not(:last-child){
  <!-- Some rules here -->
}
```

This code will select all the `p` tags but the ones that are the last child of
its parent.
