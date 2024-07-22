### <font color="#92d050">Basic CSS Syntax</font>

![[Pasted image 20240516000110.png]]

### <font color="#92d050">CSS Selectors. </font>

1. Id selector.
```css
 #heading{ background-color:blue;}
```
2. Class selector. 
   ```css
.para{ background-color:red;}
```

3. Tag/Element selector.
   ```css
h2{ background-color: yellow; }
```

4. Context selector

specify කරල තියන elements වලට විතරක් Styles apply කරන selector එකක්

example: මේකෙදි මේ style එක apply වෙන්නෙ div element එක යටතේ තියන p tag එකට විතරයි. div tag එකෙන් එලියෙ තියන p tag වලට apply වෙන්නෙ නෑ

```css
div p{color: green;}
```

5. group selector

Elements කීපයක්ම එකපාර mention කරන එක
```css
h1, h2, p {  text-align: center;  
  color: red;}
```

6. Universal Selector

The universal selector (\*) selects all HTML elements on the page.
```css
* {  text-align: center;  
  color: blue;}
```

7.  <font color="#00b0f0">element.class</font> Selector

Select and style every \<p> element with the class "intro":
```css
p.intro {  background-color: yellow;}
```


### <font color="#92d050">3 Ways to Insert CSS</font>

1. External CSS
```xml
<head>  
<link rel="stylesheet" href="mystyle.css">  
</head>
```

2. Internal CSS
```html
<head>  
  <style>  
body { background-color: linen;}  
  
h1 { color: maroon;  
  margin-left: 40px;}  
  </style>  
</head>
```

3. Inline CSS
   ```xml
<h1 style="color:blue;text-align:center;">This is a heading</h1>
```

#### <font color="#00b0f0">Also can use <font color="#e36c09">@import </font>statement as like followed.</font>

(මේකෙදි ලබා දෙන URL එකක තියන CSS file එකක් import කරන් use කරන්න පුලුවන්)
```html
<style type="text/css">
@import url("mybeautypack.css");
</style>
```

#### <font color="#ff6000">What style will be used when there is more than one style specified for an HTML element?</font>⚠

All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

### <font color="#5cff00">CSS Comments</font>

```css
/* This is a single-line comment */  
p {  color: red;}
/* This is  
a multi-line  
comment */
```

### <font color="#00b0f0">Combinators</font> 🥗
##### <font color="#00ffab">1. Descendant Selector (space) </font>
The descendant selector matches all elements that are descendants of a specified element.<font color="#ffff00">(div එක ඇතුලෙ තියන හැම P element එකකටම style එක apply වෙනවා. මේකෙදි වෙන element එකක් අස්සෙ තියන P එකකට උනත් style එක ඇප්ලයි වෙනව ඒ element එක තියෙන්නෙත් Div එක ඇතුලෙම නම්)</font>

```css
div p {
  background-color: yellow;
}
```
<br>
```html
<p>The descendant selector matches all elements that are descendants of a specified element.</p>

<div>
  <p>Paragraph 1 in the div.</p>
  <p>Paragraph 2 in the div.</p>
  <section><p>Paragraph 3 in the div.</p></section>
</div>

<p>Paragraph 4. Not in a div.</p>
<p>Paragraph 5. Not in a div.</p>
```
<span style="background:#ff4d4f">Output:</span>
![[Pasted image 20240531233718.png]]


##### <font color="#00ffab">2. Child Selector (>) </font>
The child selector (>) selects all elements that are the children of a specified element.
<font color="#ffff00">(div එක ඇතුලෙ තියන හැම P element එකකටම style එක apply වෙනවා. හැබැයි මේකෙදි වෙන element එකක් අස්සෙ තියන P එකකට style එක ඇප්ලයි වෙන්නෙ නෑ ඒ element එක තියෙන්නෙත් Div එක ඇතුලෙම උනත්)</font>
```css
div > p {  background-color: yellow;}
```
<br>
```html
<p>The child selector (>) selects all elements that are the children of a specified element.</p>

<div>
  <p>Paragraph 1 in the div.</p>
  <p>Paragraph 2 in the div.</p>
  <section>
    <!-- not Child but Descendant -->
    <p>Paragraph 3 in the div (inside a section element).</p>
  </section>
  <p>Paragraph 4 in the div.</p>
</div>

<p>Paragraph 5. Not in a div.</p>
```

<span style="background:#ff4d4f">Output:</span>
![[Pasted image 20240531234103.png]]


##### <font color="#00ffab">3. Adjacent Sibling Selector (+) </font>
adjacent sibling selector is used to select an element that is directly after another specific element.
Sibling elements must have the same parent element, and "adjacent" means "immediately following".

The following example selects the first \<p> element that are placed immediately after \<div> elements:
<font color="#ffff00">(div එක ඉවර උනාට පස්සෙ div එක ගාවම ඊලගට තියන P element එකට විතරක් style එක apply වෙනවා)</font>

```css
div + p {  background-color: yellow;}
```

```html
<p>The + selector is used to select an element that is directly after another specific element.</p>
<p>The following example selects the first p element that are placed immediately after div elements:</p>

<div>
  <p>Paragraph 1 in the div.</p>
  <p>Paragraph 2 in the div.</p>
</div>

<p>Paragraph 3. After a div.</p>
<p>Paragraph 4. After a div.</p>

<div>
  <p>Paragraph 5 in the div.</p>
  <p>Paragraph 6 in the div.</p>
</div>

<p>Paragraph 7. After a div.</p>
<p>Paragraph 8. After a div.</p>
```

<span style="background:#ff4d4f">Output:</span>
![[Pasted image 20240531234619.png]]


##### <font color="#00ffab">4. General Sibling Selector (Structure and Cascade)</font>

The general sibling selector selects all elements that are next siblings of a specified element.<font color="#ffff00">(div එකක් ඉවර උනාට පස්සෙ තියන හැම p element එකකටම style එක apply වෙනවා)</font>
```css
div ~ p {
  background-color: yellow;
}
```

```html
<p>The general sibling selector (~) selects all elements that are next siblings of a specified element.</p>

<p>Paragraph 1.</p>

<div>
  <p>Paragraph 2.</p>
</div>

<p>Paragraph 3.</p>
<code>Some code.</code>
<p>Paragraph 4.</p>

```

<span style="background:#ff4d4f">output:</span>
![[Pasted image 20240531234954.png]]





### <font color="#ff6000">CSS values and units</font>

