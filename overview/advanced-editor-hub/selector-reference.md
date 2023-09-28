# Selector reference

Selectors provide a powerful, friendly way to slice through maps,
based on [Cascading Style Sheets (CSS)](https://developer.mozilla.org/en-US/docs/Web/CSS) selectors.

If you're familiar with CSS, you'll feel right at home. If you haven't seen or used CSS, don't worry! All the selector patterns you'll ever need are documented in this reference. To see examples of how selectors can be used, check out our [general guide on selectors](/guides/selectors.md).

There are two reference tables on this page. The first shows you all the different kinds of selectors you can use in Kumu, and the second table gives details about logical operators that can be used inside of certain selectors.

In the first table, you'll notice that the word "slug" appears a lot. A [slug](/guides/slugs.md) is a piece of text that has had all letters converted to lowercase, all special characters removed, and all spaces and replaced with hyphens. So, when you see something like `type-slug` in the table below, this will be replaced in your custom selector with something like `private-company` or `individual` or another "slug" version of an element type.

## Selectors

<table id="selector-reference-table" class="table border-bottom"></table>


## Operators
<table class="table border-bottom">
  <tr>
    <th class="text-left">Operator</th>
    <th class="text-left">Description</th>
  </tr>
  <tr>
    <td><code>=</code></td>
    <td>is equal to</td>
  </tr>
  <tr>
    <td><code>!=</code></td>
    <td>is not equal to</td>
  </tr>
  <tr>
    <td><code>^=</code></td>
    <td>starts with</td>
  </tr>
  <tr>
    <td><code>$=</code></td>
    <td>ends with</td>
  </tr>
  <tr>
    <td><code>*=</code></td>
    <td>text contains</td>
  </tr>
  <tr>
    <td><code>~=</code></td>
    <td>list of values includes (this operator matches full values)</td>
  </tr>
  <tr>
    <td><code>></code></td>
    <td>is greater than</td>
  </tr>
  <tr>
    <td><code>>=</code></td>
    <td>is greater than or equal to</td>
  </tr>
  <tr>
    <td><code><</code></td>
    <td>is less than</td>
  </tr>
  <tr>
    <td><code>&lt;=</code></td>
    <td>is less than or equal to</td>
  </tr>
</table>

<table>
<thead>
<tr>
<th>Selector</th>
<th>What It Selects</th>
</tr>
</thead>
<tbody>
<tr><td><code>&#42;</code></td><td>All elements, connections, and loops</td></tr>
<tr><td><code>element</code></td><td>All elements</td></tr>
<tr><td><code>connection</code></td><td>All connections</td></tr>
<tr><td><code>loop</code></td><td>All loops</td></tr>
<tr><td><code>type-slug</code></td><td>All elements whose element type slug matches <code>type-slug</code></td></tr>
<tr><td><code>type-slug-connection</code></td><td>All connections whose connection type slug matches <code>type-slug</code></td></tr>
<tr><td><code>#label-slug</code></td><td>The item whose label slug matches <code>label-slug</code>. </td></tr>
<tr><td><code>#assigned-id-slug</code></td><td>The item whose <a href="/faq/how-do-I-avoid-duplicating-data.md">assigned ID</a> slug matches <code>assigned-id-slug</code>. </td></tr>
<tr><td><code>#system-id</code></td><td>The item whose system ID matches <code>system-id</code>. </td></tr>
<tr><td><code>.tag</code></td><td>All items whose Tags field contains <code>tag</code>. Note that this selector starts with a dot <code>.</code></td></tr>
<tr><td><code>["field name" operator "field value"]</code></td><td>All items that have a <a href="/overview/kumus-architecture.md#fields">field name and field value</a> that meet the condition of the <code>operator</code> (valid operators are listed below this table)</td></tr>
<tr><td><code>["field name"]</code></td><td>All items that have any value in the field whose name matches <code>field name</code></td></tr>
<tr><td><code>[!"field name"]</code></td><td>All items that have no value in the field whose name matches <code>field name</code></td></tr>
<tr><td><code>:from(selector)</code></td><td>All connections coming from an item that matches the <code>selector</code></td></tr>
<tr><td><code>:to(selector)</code></td><td>All connections going to an item that matches the <code>selector</code></td></tr>
<tr><td><code>:directed</code></td><td>All directed connections</td></tr>
<tr><td><code>:undirected</code></td><td>All undirected connections</td></tr>
<tr><td><code>:mutual</code></td><td>All mutual connections</td></tr>
<tr><td><code>:focus</code></td><td>All items at the root of a <a href="/guides/focus.md">focus setting</a></td></tr>
<tr><td><code>:orphan</code></td><td>All elements that have zero connections (including connections that have been filtered out)</td></tr>
<tr><td><code>:not(selector)</code></td><td>All items that do <b>not</b> match the <code>selector</code></td></tr>
<tr><td><code>:loop(selector)</code></td><td>All items that are part of a loop matching <code>selector</code></td></tr>
<tr><td><code>this-selector --&gt; that-selector</code></td><td>All items matching <code>this-selector</code> connected to items that match <code>that-selector</code></td></tr>
<tr><td><code>this-selector &lt;-- that-selector</code></td><td>All items matching <code>this-selector</code> connected from items that match <code>that-selector</code></td></tr>
<tr><td><code>this-selector &lt;--&gt; that-selector</code></td><td>All items matching <code>this-selector</code> connected to or from items that match <code>that-selector</code></td></tr>
<tr><td><code>this-selector &lt;-connection-selector-&gt; that-selector</code></td><td>All items matching <code>this-selector</code> connected to or from items that match <code>that-selector</code> via connections that match <code>connection-selector</code></td></tr>
</tbody>
</table>
