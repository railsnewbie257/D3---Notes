The <b>d3.selectAll</b> method takes a selector string, such as "circle", and returns a selection representing all 
elements that match the selector:
<pre>
<b>var</b> circle = <b>d3.selectAll</b>("circle");
</pre>

With a *selection*, we can make various changes to *selected elements*. For example, we might change the fill color 
using selection.<b>style</b> and the radius using selection.<b>attr</b>:
<pre>
circle.<b>style</b>("fill", "steelblue");
circle.<b>attr</b>("r", 30);
</pre>

The above code sets styles and attributes for all selected elements to the same values.
