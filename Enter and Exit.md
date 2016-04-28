From: https://d3js.org

Using D3’s **enter** and **exit** selections, you can create new nodes for incoming data and remove outgoing nodes that are no longer needed.from https://d3js.org

When data is bound to a selection, each element in the data array is paired with the corresponding node in the selection.
If there are fewer nodes than data, the extra data elements form the **enter** selection, which you can instantiate by 
appending to the **enter** selection. For example:
<pre>
<b>d3.select</b>("body").<b>selectAll</b>("p")
    .<b>data</b>([4, 8, 15, 16, 23, 42])
  .<b>enter</b>().<b>append</b>("p")
    .<b>text</b>(<b>function</b>(d) { return "I’m number " + d + "!"; });
</pre>

**Updating nodes are the default selection**—the result of the data operator. Thus, if you forget about the **enter** and **exit** 
selections, you will automatically select only the elements for which there exists corresponding data. 

A common pattern  is to break the initial selection into three parts: the updating nodes to modify, the entering nodes to 
add, and the exiting nodes to remove.

<pre>
// Update…
<b>var</b> p = <b>d3.select</b>("body").<b>selectAll</b>("p")
    .<b>data</b>([4, 8, 15, 16, 23, 42])
    .<b>text</b>(<b>function</b>(d) { <b>return</b> d; });

// Enter…
p.<b>enter</b>().<b>append</b>("p")
    .<b>text</b>(<b>function</b>(d) { <b>return</b> d; });

// Exit…
p.<b>exit</b>().<b>remove</b>();
</pre>

By handling these three cases separately, you specify precisely which operations run on which nodes. This improves 
performance and offers greater control over transitions. For example, with a bar chart you might initialize entering 
bars using the old scale, and then transition entering bars to the new scale along with the updating and exiting bars.

More here [Selections enter](https://github.com/mbostock/d3/wiki/Selections#enter)  
More here [Selections exit](https://github.com/mbostock/d3/wiki/Selections#exit)
