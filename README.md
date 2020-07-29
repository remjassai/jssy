<html>
<head>
  <title> 
    CSS selectors and specificity
  </title>
  <link href="SelectorsAndSpecificityHierarchy.css" rel="stylesheet" type="text/css">
</head>

<body>
  <h1>
    CSS selectors and specificity
  </h1>
<h2> Selectors </h2>
<p>In CSS, selectors are patterns used to select the element(s) you want to style.</p>
<table>
  <thead>
    <th>Selector</th>
    <th>Example</th>
    <th>Description</th>
  </thead>
  <tbody>
    <tr>
      <td><span class="code">.class</span></td>
      <td><span class="code">.intro</span></td>
      <td>Selects all elements with <span class="code">class="intro"</span></td>
    </tr>
    <tr>
      <td><span class="code">.class1.class2</span></td>
      <td><span class="code">.name1.name2</span></td>
      <td>Selects all elements with both <span class="code">name1</span> and <span class="code">name2</span> set within its <span class="code">class</span> attribute</td>
    </tr>
    <tr>
      <td><span class="code">.class1&nbsp;.class2</span></td>
      <td><span class="code">.name1&nbsp;.name2</span></td>
      <td>Selects all elements with <span class="code">name2</span> that is a descendant of an element with <span class="code">name1</span></td>
    </tr>
    <tr>
      <td><span class="code">#ID</span></td>
        <td><span class="code">#firstname</span></td>
        <td>Selects the element with <span class="code">id="firstname"</span></td>
    </tr>

    <tr>
        <td><span class="code">*</span></td>
        <td><span class="code">*</span></td>
        <td>Selects all elements</td>
    </tr>

    <tr>
        <td><span class="code">element</span></td>
        <td><span class="code">p</span></td>
        <td>Selects all <span class="code">&ltp&gt</span> elements</td>
    </tr>

    <tr>
        <td><span class="code">element.class</span></td>
        <td><span class="code">p.intro</span></td>
        <td>Selects all <span class="code">&ltp&gt</span> elements with <span class="code">class="intro"</span></td>
    </tr>
    <tr>
        <td><span class="code">element,element</span></td>
        <td><span class="code">div, p</span></td>
        <td>Selects all <span class="code">&ltdiv&gt</span> elements and all <span class="code">&ltp&gt</span> elements</td>
    </tr>

    <tr>
        <td><span class="code">element element</span></td>
        <td><span class="code">div p</span></td>
        <td>Selects all <span class="code">&ltp&gt</span> elements inside <span class="code">&ltdiv&gt</span> elements</td>
    </tr>

    <tr>
        <td><span class="code">element&nbsp;&gt&nbsp;element</span></td>
        <td><span class="code">div&nbsp;&gt&nbsp;p</span></td>
        <td>Selects all <span class="code">&ltp&gt</span> elements where the parent is a <span class="code">&ltdiv&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">element+element</span></td>
        <td><span class="code">div + p</span></td>
        <td>Selects all <span class="code">&ltp&gt</span> elements that are placed immediately after <span class="code">&ltdiv&gt</span> elements</td>
    </tr>

    <tr>
        <td><span class="code">element1~element2</span></td>
        <td><span class="code">p ~ ul</span></td>
        <td>Selects every <span class="code">&ltul&gt</span> element that are preceded by a <span class="code">&ltp&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">[attribute]</span></td>
        <td><span class="code">[target]</span></td>
        <td>Selects all elements with a <span class="code">target</span> attribute</td>
    </tr>

    <tr>
        <td><span class="code">[attribute=value]</span></td>
        <td><span class="code">[target=_blank]</span></td>
        <td>Selects all elements with <span class="code">target="_blank"</span></td>
    </tr>

    <tr>
        <td><span class="code">[attribute~=value]</span></td>
        <td><span class="code">[title~=flower]</span></td>
        <td>Selects all elements with a <span class="code">title</span> attribute containing the word "flower"</td>
    </tr>
    <tr>
        <td><span class="code">[attribute|=value]</span></td>
        <td><span class="code">[lang|=en]</span></td>
        <td>Selects all elements with a <span class="code">lang</span> attribute value starting with "en"</td>
    </tr>

    <tr>
        <td><span class="code">[attribute^=value]</span></td>
        <td><span class="code">a[href^="https"]</span></td>
        <td>Selects every <span class="code">&lta&gt</span> element whose <span class="code">href</span> attribute value begins with "https"</td>
    </tr>
    <tr>
        <td><span class="code">[attribute$=value]</span></td>
        <td><span class="code">a[href$=".pdf"]</span></td>
        <td>Selects every <span class="code">&lta&gt</span> element whose <span class="code">href</span> attribute value ends with ".pdf"</td>
    </tr>
    <tr>
        <td><span class="code">[attribute*=value]</span></td>
        <td><span class="code">a[href*="w3schools"]</span></td>
        <td>Selects every <span class="code">&lta&gt</span> element whose <span class="code">href</span> attribute value contains the substring "w3schools"</td>
    </tr>
    <tr>
        <td><span class="code">:active</span></td>
        <td><span class="code">a:active</span></td>
        <td>Selects the active link</td>
    </tr>
    <tr>
        <td><span class="code">::after</span></td>
        <td><span class="code">p::after</span></td>
        <td>Insert something after the content of each <span class="code">&ltp&gt</span> element</td>
    </tr>

    <tr>
        <td><span class="code">::before</span></td>
        <td><span class="code">p::before</span></td>
        <td>Insert something before the content of each <span class="code">&ltp&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:checked</span></td>
        <td><span class="code">input:checked</span></td>
        <td>Selects every checked <span class="code">&ltinput&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:default</span></td>
        <td><span class="code">input:default</span></td>
        <td>Selects the default <span class="code">&ltinput&gt</span> element</td>
    </tr>

    <tr>
        <td><span class="code">:disabled</span></td>
        <td><span class="code">input:disabled</span></td>
        <td>Selects every disabled <span class="code">&ltinput&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:empty</span></td>
        <td><span class="code">p:empty</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that has no children (including text nodes)</td>
    </tr>

    <tr>
        <td><span class="code">:enabled</span></td>
        <td><span class="code">input:enabled</span></td>
        <td>Selects every enabled <span class="code">&ltinput&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:first-child</span></td>
        <td><span class="code">p:first-child</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the first child of its parent</td>
    </tr>
    <tr>
        <td><span class="code">::first-letter</span></td>
        <td><span class="code">p::first-letter</span></td>
        <td>Selects the first letter of every <span class="code">&ltp&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">::first-line</span></td>
        <td><span class="code">p::first-line</span></td>
        <td>Selects the first line of every <span class="code">&ltp&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:first-of-type</span></td>
        <td><span class="code">p:first-of-type</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the first <span class="code">&ltp&gt</span> element of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:focus</span></td>
        <td><span class="code">input:focus</span></td>
        <td>Selects the <span class="code">&ltinput&gt</span> element which has focus</td>
    </tr>
    <tr>
        <td><span class="code">:hover</span></td>
        <td><span class="code">a:hover</span></td>
        <td>Selects links on mouse over</td>
    </tr>

    <tr>
        <td><span class="code">:in-range</span></td>
        <td><span class="code">input:in-range</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with a value within a specified rangev</td>
    </tr>

    <tr>
        <td><span class="code">:indeterminate</span></td>
        <td><span class="code">input:indeterminate</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements that are in an indeterminate state</td>
    </tr>
    <tr>
        <td><span class="code">:invalid</span></td>
        <td><span class="code">input:invalid</span></td>
        <td>Selects all <span class="code">&ltinput&gt</span> elements with an invalid value</td>
    </tr>

    <tr>
        <td><span class="code">:lang(language)</span></td>
        <td><span class="code">p:lang(it)</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element with a lang attribute equal to "it" (Italian)</td>
    </tr>
    <tr>
        <td><span class="code">:last-child</span></td>
        <td><span class="code">p:last-child</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the last child of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:last-of-type</span></td>
        <td><span class="code">p:last-of-type</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the last <span class="code">&ltp&gt</span> element of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:link</span></td>
        <td><span class="code">a:link</span></td>
        <td>Selects all unvisited links</td>
    </tr>
    <tr>
        <td><span class="code">:not(selector)</span></td>
        <td><span class="code">:not(p)</span></td>
        <td>Selects every element that is not a <span class="code">&ltp&gt</span> element</td>
    </tr>
    <tr>
        <td><span class="code">:nth-child(n)</span></td>
        <td><span class="code">p:nth-child(2)</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the second child of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:nth-last-child(n)</span></td>
        <td><span class="code">p:nth-last-child(2)</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the second child of its parent, counting from the last child</td>
    </tr>
    <tr>
        <td><span class="code">:nth-last-of-type(n)</span></td>
        <td><span class="code">p:nth-last-of-type(2)</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the second <span class="code">&ltp&gt</span> element of its parent, counting from the last child</td>
    </tr>
    <tr>
        <td><span class="code">:nth-of-type(n)</span></td>
        <td><span class="code">p:nth-of-type(2)</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the second <span class="code">&ltp&gt</span> element of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:only-of-type</span></td>
        <td><span class="code">p:only-of-type</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the only <span class="code">&ltp&gt</span> element of its parent</td>
    </tr>

    <tr>
        <td><span class="code">:only-child</span></td>
        <td><span class="code">p:only-child</span></td>
        <td>Selects every <span class="code">&ltp&gt</span> element that is the only child of its parent</td>
    </tr>
    <tr>
        <td><span class="code">:optional</span></td>
        <td><span class="code">input:optional</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with no "required" attribute</td>
    </tr>
    <tr>
        <td><span class="code">:out-of-range</span></td>
        <td><span class="code">input:out-of-range</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with a value outside a specified range</td>
    </tr>
    <tr>
        <td><span class="code">::placeholder</span></td>
        <td><span class="code">input::placeholder</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with the "placeholder" attribute specified</td>
    </tr>
    <tr>
        <td><span class="code">:read-only</span></td>
        <td><span class="code">input:read-only</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with the "readonly" attribute specified</td>
    </tr>
    <tr>
        <td><span class="code">:read-write</span></td>
        <td><span class="code">input:read-write</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with the "readonly" attribute NOT specified</td>
    </tr>
    <tr>
        <td><span class="code">:required</span></td>
        <td><span class="code">input:required</span></td>
        <td>Selects <span class="code">&ltinput&gt</span> elements with the "required" attribute specified</td>
    </tr>
    <tr>
        <td><span class="code">:root</span></td>
        <td><span class="code">:root</span></td>
        <td>Selects the document's root element</td>
    </tr>
    <tr>
        <td><span class="code">::selection</span></td>
        <td><span class="code">::selection</span></td>
        <td>Selects the portion of an element that is selected by a user</td>
    </tr>
    <tr>
        <td><span class="code">:target</span></td>
        <td><span class="code">#news:target</span></td>
        <td>Selects the current active <span class="code">#news</span> element (clicked on a URL containing that anchor name)</td>
    </tr>

    <tr>
        <td><span class="code">:valid</span></td>
        <td>input:valid</span></td>
        <td>Selects all <span class="code">&ltinput&gt</span> elements with a valid value</td>
    </tr>
    <tr>
        <td><span class="code">:visited</span></td>
        <td><span class="code">a:visited</span></td>
        <td>Selects all visited links</td>
    </tr>

  </tbody>
</table>

<h2> Specificity Hierarchy </h2>

<p>Every selector has its place in the specificity hierarchy. Four categories define the specificity level, so think of specificity as a score/rank system that determines which style declarations apply to an element.</p>

<table>

<thead>
  <th>Selector</th>
  <th>Example</th>
  <th>Level</th>
  <th>Description</th>
</thead>
<tbody>
  <tr>
    <td>Inline Styles</td>
    <td><span class="code">&lth1 style="color: #ffffff;"&gt</span></td>
    <td>1000</td>
    <td>An inline style is attached directly to the element to be styled.</td>
  </tr>
  <tr>
    <td>IDs</td>
    <td><span class="code">#navbar</span></td>
    <td>100</td>
    <td>An ID is a unique identifier for the page elements.</td>
  </tr>
  <tr>
    <td>Classes, Attributes and Pseudo-classes</td>
    <td><span class="code">.classes, [attributes]</span> and <span class="code">:hover</span></td>
    <td>10</td>
    <td></td>
  </tr>
  <tr>
    <td>Elements and Pseudo-Elements</td>
    <td><span class="code">h1</span> and <span class="code">:before</span></td>
    <td>1</td>
    <td></td>
  </tr>


</tbody>

</table>



</body>

<foot>

</foot>
</html>
