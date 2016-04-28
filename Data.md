<b>Data</b> is specified as an ***array of values***; this mirrors the concept of a <b>selection</b>, which is an array 
of elements.
<pre>
circle.<b>data</b>([32, 57, 112]);
</pre>

After data is bound, it is accessible as the **first argument to attribute and style functions**. 

By convention, we typically use the name <b>d</b> to refer to bound data

<pre>
circle.<b>attr</b>("r", <b>function</b>(d) { <b>return Math.sqrt</b>(d); });
</pre>

More at [Selections data](https://github.com/mbostock/d3/wiki/Selections#data)
