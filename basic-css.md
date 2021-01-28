<h1 class="capitalize">COMD2451</h1>
<h2 class=" capitalize center">Basic CSS</h2>

---

<section class="section">
    <h2 class="sentence">So what is CSS anyway?</h2>

`CSS` ***stands*** for `Cascading StyleSheets`.

`CSS` is the ***language*** for ***describing*** the `presentation` of `web pages`. That ***includes*** `colors`, `layout`, and `fonts`. It ***allows*** for the ***adaption*** of `presentation` to ***different*** types of ***devices***, such as `large screens`, `small screens`, or `printers`.

`CSS` is ***independent*** of `HTML`, and the ***separation*** of `HTML` from `CSS` makes it ***easier*** to ***maintain*** sites, ***share*** style sheets ***across*** pages, and ***tailor*** pages to ***different*** environments. This is ***referred*** to as the `separation of structure` (or `content`) from `presentation`.

</section>

---

<section class="section">
    <h2 class="sentence">So what does Cascading mean?</h2>

`Cascading` ***means*** that a `style` ***applied*** to a `parent element` will ***also*** apply to ***all*** `children elements` ***within*** the `parent`.

For ***example***, if you ***set*** the `color` of ***text*** within the `body` element to `red`, ***all*** `headings`, `paragraphs`, and ***other*** `text elements` ***within*** the `body` will ***also*** be the `color` ***red*** (***unless*** something ***else*** is ***specified***).

```css
body {
    color: red;
}
```

</section>

---

<section class="section">
    <h2 class="sentence">The CSS Selector</h2>

When ***learning*** `CSS`, the ***first*** `CSS` term one should ***tackle*** is the `CSS` selector.

A `CSS` selector ***specifies*** which `element`(s) ***within*** the `HTML` document to ***target*** and apply ***styles*** to.

According to [Shay Howe](https://learn.shayhowe.com/html-css/building-your-first-web-page/),

> Selectors generally target an attribute `value`, such as an `id` or `class` value, or target the `type` of `element`, such as `<h1>` or `<p>`.

One can get ***very*** specific as to ***which*** particular `element`, or `attribute` value, for ***example***, one wants to ***target***, or be as ***general*** as targeting ***all*** instances of a ***particular*** `element`.

For ***example***, if one ***wanted*** to target ***all*** instances of the `a` (`anchor`) element on a ***page***, one would ***start*** by doing the ***following***:

```css
a {

}
```

The `a` ***represents*** the `element selector`, as it ***targets*** the `a` (`anchor`) element on the `HTML` page. If it is ***simply*** written in ***this*** manner, ***all*** `a` elements on the `HTML` page will be `styled` ***according*** to the the `properties` and their `values` ***defined*** inside the `a` element `selector`.

</section>

---

<section class="section">
    <h2 class="sentence">How CSS Selectors are Defined</h2>

`CSS` selectors are ***defined*** by ***first*** indicating the `CSS` selector, ***followed*** by an ***opening*** `{` and ***closing*** `}` curly brace.

```css
a {

}
```

</section>

---

<section class="section">
    <h2 class="sentence">CSS Properties and Their Declarations</h2>

A `CSS` property ***styles*** an ***aspect*** of an `HTML` element. For ***example***, the `color` property will ***style*** the `color` of the `element`.

```css
a {
    color: pink;
}
```

The `name` of the `property` ***above*** is `color`, and its `value` is `pink`. This ***means*** that the `color` of ***all*** `a` elements on the `HTML` page will be `pink`.

`color: pink;` is referred to as a `property declaration`. A `property declaration` ***consists*** of a `property name` and its ***corresponding*** `value`. 

A `property declaration` should ***always*** `end` with a `:` ***semi-colon***.

</section>

---

<section class="section">
    <h2 class="sentence">The CSS Rule Set</h2>

A `rule set` is a ***single*** section of `CSS` ***including*** the `selector`, the `curly braces`, and ***lines*** containing `property declarations` (`properties` and their `values`).

```css
a {
    color: pink;
    text-decoration: none;
}
```

***Here***, the [text-decoration](https://www.w3schools.com/cssref/pr_text_text-decoration.asp) ***property***, which ***specifies*** the decoration to ***add*** to text, has been ***given*** the `value` of `none`, which ***means*** that `a` elements will ***not*** be `underlined` or contain ***any*** other ***kind*** of `text decoration`.

It is ***important*** to ***note*** that if a `property declaration` is ***made*** inside a ***particular*** `rule set` of a `CSS selector` ***earlier*** in the `CSS` ***style sheet***, and then the ***same*** `CSS` selector `rule set`'s `property declaration(s)` are `modified` ***later***(***lower*** down) in the `style sheet`, the `property declarations` ***lower*** down the `style sheet` will ***override*** the `declarations` made ***earlier*** on (***higher*** up) in the `style sheet`.

That's ***why*** it is ***important*** to have ***DRY*** `CSS`. `DRY` ***stands*** for `Don't Repeat Yourself`.

</section>

---

<section class="section">
    <h2 class="sentence">The CSS Declaration Block</h2>

A `CSS declaration block` is the ***section*** of `CSS` which ***contains*** the `property names` and their `values`. In ***other*** words, they are the ***lines*** which appear ***between*** the opening `{` and closing `}` ***curly braces***.

```css
color: pink;
text-decoration: none;
```

</section>

---

<section class="section">
    <h2 class="sentence">The Element Type Selector</h2>

An `element type selector` is a `selector` which ***targets*** an `element` by its `element` ***name***.

```css
section {
    background: purple;
}
```

</section>

---

<section class="section">
    <h2 class="sentence">The Class Selector</h2>

The `class selector` ***targets*** an `element` by its `class name`. ***Every*** `element` with the ***same*** `class name` will ***receive*** the `styles` ***set*** in the `property declarations` of the ***particular*** `rule set` in ***question***.

```css
.para {
    font-size: 1.5rem;
    /* CSS rule to specify the font family  (aka property dec;ration) */
    font-family: font-family: 'Open Sans', sans-serif;
}
```

</section>

---

<section class="section">
    <h2 class="sentence">Specifying only a specific element for a class</h2>

One can ***also*** specify that only ***specific*** `element`(s) should be ***specified*** by a `class`.

```css
p.center {
    text-align: center;
}
```

***This*** way, if an `h1` element ***also*** contains the `.center` ***class***, for ***example***, ***only*** the `p` element with the `.center` ***class*** will be ***affected***.

</section>

---

<section class="section">
    <h2 class="sentence">The id Selector</h2>

The `id selector` ***targets*** an `element` by its `id`. The `element` with a certain ***unique*** `id` will ***receive*** the `styles` ***set*** in the `property declarations` of the ***particular*** `rule set` in ***question***.

```css
#main-header {
    text-align: center;
}
```

</section>

---

<section class="section">
    <h2 class="sentence">The Universal Selector</h2>

The `universal selector` ***represented*** by `*` (`asterisk`) selects ***all*** `HTML` elements on the ***page***.

For ***example***, I ***use*** the `universal selector` to ***create*** my ***own*** `custom CSS reset`. ***Typically***, I create the ***following*** `rule set`:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

I will ***discuss*** what this ***means*** when we ***cover*** `CSS resets`. But for the ***purpose*** of ***describing*** what the `universal selector` is ***doing*** in this ***instance***, it ***applies*** the `property declarations` ***inside*** the `declaration block` to ***all*** the `elements` on the `HTML` ***page***.

</section>

---

<section class="section">
    <h2 class="sentence">The Grouping Selector</h2>

The `grouping selector` selects ***all*** the `HTML` elements with the ***same*** `style` ***definitions***.

```css
h1 {
    text-align: center;
}

p {
    text-align: center;
}
```

So that there ***isn't*** any ***repetition*** of `CSS` going on, ***instead***, I do the ***following***:

```css
h1, p {
    text-align: center;
}
```

</section>

---

<section class="section">
    <h2 class="sentence">The Attribute Selector</h2>

An `attribute selector` ***selects*** an `element` to ***target*** based on an `HTML` attribute `name` and/or its `value`.

***Selecting*** an `element` to ***target*** based on the `element` and its `attribute name` ***alone***:

```css
input[name] {
    color: blue;
}
```

***Here***, we are ***selecting*** the `input` element to ***target*** by the `name` of the `name attribute`.

```css
input[name="email"] {
    background: #ffdbab;
}
```

***Here***, we are ***selecting*** the `input` element to ***target*** by the `element`'s `name attribute` ***and*** its ***specific*** `value`. This is ***usually*** seen when ***styling*** `forms`, where the `input` element with the `name` attribute and the `value` of `"email"` would be ***found*** in `forms`. These `inputs` are also ***referred*** to as `form controls`. We will be ***discussing*** this in ***more*** detail when we ***work*** with `forms` later ***on***.

</section>

---

<section class="section">
    <h2 class="sentence">CSS Selector Categories</h2>

`CSS` ***selectors*** can be ***separated*** into [5 categories](https://www.w3schools.com/css/css_selectors.asp):

+ `Simple selectors` (select elements based on name, id, or class)

+ `Combinator selectors` (select elements based on a specific relationship between them)

+ `Pseudo-class selectors` (select elements based on a certain state)

+ `Pseudo-element selectors` (select and style a part of an element)

+ `Attribute selectors` (select elements based on an attribute or attribute value)

</section>

---

<section class="section">
    <h2 class="sentence">CSS Simple Selectors</h2>

So far, we have gone over all the [simple selectors](https://www.w3schools.com/css/css_selectors.asp):

+ The `element type` selector

+ The `class` selector

+ The `id` selector

+ Selecting ***specific*** `elements` by ***class***

+ The `universal` selector

+ The `grouping` selector

We ***also*** briefly covered the `attribute` selector ***category***, because we ***touched*** upon the `element attribute` when covering ***basic*** `HTML`. We will get into the ***other*** 3 categories ***later*** on.

</section>

---

<section class="section">
    <h2 class="sentence">The 3 ways of adding CSS to HTML documents</h2>

`CSS` can be ***added*** to `HTML` documents in ***three*** ways:

+ `inline` - by ***using*** the `style` attribute ***inside*** `HTML` elements in `HTML` documents

+ `internal` - by ***using*** the `style` element in the `head` ***section*** of an `HTML` document

+ `external` - by ***using*** a `link` element ***inside*** the `head` element to ***link*** to an ***external*** `CSS` file

</section>

---

<section class="section">
    <h2 class="sentence">Inline CSS</h2>

`Inline CSS` is `CSS` that is placed ***within*** the `opening tag` of an `HTML` element ***located*** inside the `HTML` document, ***using*** the `style` attribute.

```html
<p style="text-align: center">
```

***Instead*** of ***selecting*** the `p` element by its `name`, `class`, or `id`, ***inside*** an ***external*** `style sheet` ***or*** the `style` element, we ***style*** it ***using*** the `style` attribute `inline`. 

</section>

---

<section class="section">
    <h2 class="sentence">Internal CSS</h2>

`Internal CSS` is ***used*** to ***style*** an ***individual*** `HTML` page.

`Internal CSS` is ***defined*** within the `head` element, and it ***uses*** the `style` element.

```html
<style>
  p {
    text-align: center;
  }
</style>
```

It's a ***bit*** better than ***using*** `inline CSS`, since it ***can*** `style` ***all*** the `p` elements on the `HTML` page ***instead*** of just ***one*** specific `p` element, but ***using*** `inline` or `internal CSS` ***potentially*** means ***repeating*** `CSS` ***over*** and ***over***.

With `inline CSS`, it ***means*** potentially ***repeating*** the `inline CSS` using the `style` attribute in ***all*** `p` elements which ***require*** that ***particular*** styling.

With `internal CSS`, it ***means*** potentially ***copying*** and ***pasting*** the `style` element and its ***contents*** in ***all*** the `HTML` pages where the styling ***defined*** within the `style` element is ***required***.

</section>

---

<section class="section">
    <h2 class="sentence">External CSS</h2>

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>How I created my first html web page</h1>
    </header>
    <main>
        <article>
            <h2>Creating the index.html file</h2>
            <p>First I created a file called "index.html" with the touch command inside the root of my project folder
                from Terminal.</p>
        </article>
    </main>
</body>
</html>
```

`External CSS` means ***using*** an `external style sheet` to ***define*** the `style` for ***many*** `HTML` ***pages***.

To ***use*** an ***external*** `style sheet`, we ***add*** a `link` element to the `head` of the `HTML` document ***using*** the `rel` and the `href` attributes ***inside*** the `link` element and ***adding*** it to the `head` of ***each*** `HTML` ***page*** we want to ***style*** with that ***particular*** `style sheet`.

Doing it in ***this*** manner ***saves*** a ***lot*** of ***time*** and ***work***, because an ***external*** `style sheet` ***controls*** the `layout` of ***multiple*** pages at ***once***, and making `style` ***changes*** is ***much*** easier and ***faster***.

</section>

---

<section class="section">
    <h2 class="sentence">Related Resources</h2>

+ [What is CSS?: W3.org](https://www.w3.org/standards/webdesign/htmlcss.html)

+ [Building Your First Web Page (CSS): Shay Howe](https://learn.shayhowe.com/html-css/building-your-first-web-page/)

+ [CSS Terms and Definitions: Impressive Web](https://www.impressivewebs.com/css-terms-definitions/)

+ [CSS Selectors: w3schools](https://www.w3schools.com/css/css_selectors.asp)

+ [Common CSS Properties Reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)

+ [CSS Properties and CSS Rules: Jacob Jenkov](http://tutorials.jenkov.com/css/css-properties-css-rules.html)

+ [CSS Snapshot 2020 W3C Working Group Note, 22 December 2020](https://www.w3.org/TR/CSS/#css)

+ [HTML Styles - CSS: w3schools](https://www.w3schools.com/html/html_css.asp)

+ [What is a form control in HTML?: stackoverflow](https://stackoverflow.com/questions/31739685/what-is-a-form-control-in-html)

+ [Beginner Concepts: How CSS Selectors Work: CSS Tricks](https://css-tricks.com/how-css-selectors-work/)

</section>