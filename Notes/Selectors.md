# Selectors

<h2><b>Relational Selector</b></h2>

 * `ul li` tells us that we want to select the element `li` which is a descendant of the element `ul`. The space in between the two elements indicates that the second element is a descendant of the first element.

 * `ol > li` tells us that we want to select the element `li` which is a child of the element `ol`. The 'greater than' sign shows that the second element is a child of the first element.

<hr/>
<h4><i>Child vs Descendant</i></h3>

```html
<div>
    <a href="#">
        <p>link</p>
    </a>
</div>
```
In our snippet up here the `p` element is only a descendant of the `div` element, where as the `a` element is a child of the `div` element. The child element is directly below the parent element in the DOM, where as a descendant can be a few elements removed. 

Note that when we use the child selector on `a`, the `p` element will also be selected as part of the `a` element. (What about descendant selectors?)

<hr/>

 * `li.className + li` this means we want to select the `li` element that comes immediately after the `li` element with the class `className`.

 * `li.className ~ li` means that we want to select all the `li` elements that come after `li.className`.

<br/>

<h2><b>Attribute Selectors</b></h3>

These select the attribute of an element. They follow a general structure: `element[attribute]`.

E.g
```html
<img src="image.jpg" alt="accessible">
```
```css
img[alt] {}
```

In the example above we can see that in our css we are selecting the `alt` attribute of the `img` element.

Attribute selectors gives us the ability to choose how targeted we are in our selection. For example: 

* `element[attribute="val"]` allows us to select an element with an attribute contains the value "val".

* `element[attribute |= val]` means that we want to select an element that has an attribute that have the value "val" or begins with "val".

* `element[attribute ^= val]` means select element which has an attribute *attribute* starts with val.

* `element[attribute $= val]` means select element which has an attribute *attribute* ends with val.

* `element[attribute *= val]` means select element which has an attribute *attribute* that has the string val anywhere within it.