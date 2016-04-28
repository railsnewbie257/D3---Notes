We can also set values on a per-element basis by using **anonymous functions**. The function is evaluated once per 
selected element. **Anonymous functions** are used extensively in D3 to compute attribute values, particularly in 
conjunction with **scales** and **shapes**. To set each circle’s x-coordinate to a random value:
<pre>
circle.<b>attr</b>("cx", <b>function</b>() { <b>return Math.random</b>() * 720; });
</pre>

From: https://bost.ocks.org/mike/circles/
