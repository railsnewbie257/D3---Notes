###Rectangle Example
<pre>
// Rectangle data
<b>var</b> jsonRectangles = [
  { "x_axis": 10, "y_axis": 10, "height": 20, "width":20, "color" : "green" },
  { "x_axis": 40, "y_axis": 40, "height": 20, "width":20, "color" : "purple" },
  { "x_axis": 70, "y_axis": 70, "height": 20, "width":20, "color" : "red" }];

// Build a container
<b>var</b> svgContainer = <b>d3.select</b>("body").<b>append</b>("svg")
                                    .<b>attr</b>("width", 100)
                                    .<b>attr</b>("height", 100);

// Add the data for rectangles
<b>var</b> rectangles = svgContainer.<b>selectAll</b>("rect")
                             .<b>data</b>(jsonRectangles)
                             .<b>enter</b>()
                             .<b>append</b>("rect");

// Style the rectangles
<b>var</b> rectangleAttributes = rectangles
                          .<b>attr</b>("x", <b>function</b> (d) { <b>return</b> d.x_axis; })
                          .<b>attr</b>("y", <b>function</b> (d) { <b>return</b> d.y_axis; })
                          .<b>attr</b>("height", <b>function</b> (d) { <b>return</b> d.height; })
                          .<b>attr</b>("width", <b>function</b> (d) { <b>return</b> d.width; })
                          .<b>style</b>("fill", <b>function</b> (d) { <b>return</b> d.color; });
</pre>
