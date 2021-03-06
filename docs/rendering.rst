
  .. image:: ../artwork/toyplot.png
    :width: 200px
    :align: right
  
.. _rendering:

Rendering
---------

Of course, any plotting library needs a way to render figures for
display, and Toyplot is no exception. To integrate Toyplot into your
workflow as easily as possible, we provide three different rendering
mechanisms:

Backends
~~~~~~~~

At the lowest level, Toyplot provides a large collection of rendering
``backends``. Each backend knows how to render a Toyplot canvas to a
specific file format, and can typically render the canvas directly to
disk, to a buffer you provide, or return the raw representation of the
canvas for further processing. You choose a backend that provides the
file format you want to generate, and use it to explicitly render your
canvas. For example, you could use the :mod:`toyplot.pdf` backend to
save a figure as a vector PDF image on disk:

.. code:: python

    import toyplot.pdf
    toyplot.pdf.render(canvas, "figure1.pdf")

Similarly, you could substitute the :mod:`toyplot.png` backend to save
a PNG bitmap image:

.. code:: python

    import toyplot.png
    toyplot.png.render(canvas, "figure1.png")

You could do the same with the :mod:`toyplot.svg` backend, but suppose
you wanted to add a custom CSS class to the SVG markup for inclusion in
a publishing workflow. To accomodate this, the SVG backend can return a
DOM for further editing, instead of saving it directly to disk:

.. code:: python

    import toyplot.svg
    svg = toyplot.svg.render(canvas)
    svg.attrib["class"] = "MyCustomClass"
    import xml.etree.ElementTree as xml
    with open("figure1.svg", "wb") as file:
        file.write(xml.tostring(svg))

Finally, there is Toyplot's most important backend,
:mod:`toyplot.html` which produces the preferred interactive HTML
representation of a canvas. Like the other backends, you can use it to
write directly to disk, or return a DOM object for editing as-needed:

.. code:: python

    import toyplot.html
    toyplot.html.render(canvas, "figure1.html")

Note that the file produced by this backend is a completely
self-contained HTML fragment that could be emailed directly to a
colleague, inserted into a larger HTML document, etc.

Displays
~~~~~~~~

While backends are useful when you wish to save a canvas to disk for
incorporation into a paper or some larger workflow, in many cases you
may find yourself simply wanting to display the results of some
computation. Writing files to disk and opening them in a separate
application can be time-consuming and frustrating, particularly when
running a script repeatedly during development. For this case, Toyplot
provides ``display`` modules, which provide convenient ways to display
figures interactively. The most portable of these modules is
:mod:`toyplot.browser`:

.. code:: python

    import toyplot.browser
    toyplot.browser.show(canvas)

This will open a new browser window containing your figure, with all of
Toyplot's interaction and features intact.

If you prefer, an experimental new Qt display is available. It also
displays figures in a popup window with full interaction; in the future
it may grow to include additional Toyplot-specific functionality:

.. code:: python

    import toyplot.qt
    toyplot.qt.show(canvas)

Autorendering
~~~~~~~~~~~~~

For interactive environments such as
`Jupyter <http://www.ipython.org>`__, Toyplot's *autorender* feature
automatically renders a canvas into a notebook cell using Toyplot's
preferred interactive HTML representation. We use autorendering with few
exceptions throughout this documentation ... for example, executing the
following automatically inserts a figure into a Jupyter notebook:

.. code:: python

    import numpy
    x = numpy.linspace(0, 1)
    y = x ** 2

.. code:: python

    import toyplot
    canvas = toyplot.Canvas(width=300)
    canvas.axes().plot(x, y);



.. raw:: html

    <div align="center" class="toyplot" id="t794f466b7c9245139e15937d734b2294"><svg height="300.0px" id="t4ade6d85cf5a4379a193df5f50fcf4b3" preserveAspectRatio="xMidyMid meet" style="background-color:transparent;fill:rgb(16.1%,15.3%,14.1%);fill-opacity:1.0;font-family:helvetica;font-size:12px;opacity:1.0;stroke:rgb(16.1%,15.3%,14.1%);stroke-opacity:1.0;stroke-width:1.0" viewBox="0 0 300.0 300.0" width="300.0px" xmlns="http://www.w3.org/2000/svg" xmlns:toyplot="http://www.sandia.gov/toyplot"><g class="toyplot-axes-Cartesian" id="t6d296b08f9a84104a55fa2d499c320ae"><clipPath id="tb5a940e53692452f8449c11b03f4d13d"><rect height="200.0" width="200.0" x="50.0" y="50.0"></rect></clipPath><g class="toyplot-coordinate-events" clip-path="url(#tb5a940e53692452f8449c11b03f4d13d)" style="cursor:crosshair"><rect height="200.0" style="pointer-events:all;visibility:hidden" width="200.0" x="50.0" y="50.0"></rect><g class="toyplot-mark-Plot" id="tad1f8a1c0bab48f4a1c60839146c3f6c" style="fill:none"><g class="toyplot-Series"><path d="M 60.0 240.0 L 63.673469387755105 239.92503123698458 L 67.346938775510196 239.70012494793838 L 71.020408163265316 239.32528113286131 L 74.693877551020407 238.80049979175345 L 78.367346938775512 238.12578092461476 L 82.040816326530617 237.30112453144525 L 85.714285714285722 236.32653061224491 L 89.387755102040813 235.20199916701375 L 93.061224489795919 233.92753019575176 L 96.734693877551024 232.50312369845898 L 100.40816326530611 230.92877967513536 L 104.08163265306122 229.20449812578093 L 107.75510204081633 227.33027905039569 L 111.42857142857143 225.30612244897958 L 115.10204081632654 223.13202832153269 L 118.77551020408163 220.80799666805498 L 122.44897959183673 218.33402748854647 L 126.12244897959184 215.71012078300706 L 129.79591836734693 212.93627655143689 L 133.46938775510205 210.01249479383591 L 137.14285714285714 206.9387755102041 L 140.81632653061223 203.71511870054144 L 144.48979591836735 200.341524364848 L 148.16326530612244 196.81799250312369 L 151.83673469387756 193.1445231153686 L 155.51020408163265 189.3211162015827 L 159.18367346938777 185.34777176176596 L 162.85714285714286 181.2244897959184 L 166.53061224489795 176.95127030403995 L 170.20408163265304 172.5281132861308 L 173.87755102040813 167.95501874219076 L 177.55102040816325 163.2319866722199 L 181.22448979591837 158.35901707621824 L 184.89795918367346 153.33610995418576 L 188.57142857142856 148.16326530612247 L 192.24489795918367 142.84048313202834 L 195.91836734693877 137.36776343190337 L 199.59183673469389 131.74510620574762 L 203.26530612244895 125.97251145356105 L 206.93877551020407 120.04997917534362 L 210.61224489795916 113.97750937109539 L 214.28571428571428 107.75510204081634 L 217.9591836734694 101.38275718450647 L 221.63265306122446 94.860474802165797 L 225.30612244897955 88.188254893794294 L 228.9795918367347 81.366097459391938 L 232.65306122448979 74.39400249895877 L 236.32653061224491 67.271970012494791 L 240.0 60.0" style="fill:none;stroke:rgb(40%,76.1%,64.7%);stroke-opacity:1.0;stroke-width:2.0"></path></g></g></g><g class="toyplot-coordinates" style="visibility:hidden"><rect height="14.0" style="fill:rgb(100%,100%,100%);fill-opacity:1.0;opacity:0.75;stroke:none" width="90.0" x="150.0" y="60.0"></rect><text style="alignment-baseline:middle;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="195.0" y="67.0"></text></g><line style="" x1="60.0" x2="240.0" y1="250.0" y2="250.0"></line><g><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="60.0" y="250.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="150.0" y="250.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="240.0" y="250.0">1.0</text></g><line style="" x1="50.0" x2="50.0" y1="60.0" y2="240.0"></line><g><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50.0, 240.0)" x="50.0" y="240.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50.0, 150.0)" x="50.0" y="150.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50.0, 60.0)" x="50.0" y="60.0">1.0</text></g></g></svg><div class="toyplot-controls"><ul class="toyplot-mark-popup" onmouseleave="this.style.visibility='hidden'" style="background:rgba(0%,0%,0%,0.75);border:0;border-radius:6px;color:white;cursor:default;list-style:none;margin:0;padding:5px;position:fixed;visibility:hidden"><li class="toyplot-mark-popup-title" style="color:lightgray;cursor:default;padding:5px;list-style:none;margin:0;"></li><li class="toyplot-mark-popup-save-csv" onmouseout="this.style.color='white';this.style.background='steelblue'" onmouseover="this.style.color='steelblue';this.style.background='white'" style="border-radius:3px;padding:5px;list-style:none;margin:0;">Save as .csv</li></ul><script>
    (function()
    {
      if(window.CSS !== undefined && window.CSS.supports !== undefined)
      {
        if(!window.CSS.supports("alignment-baseline", "middle"))
        {
          var re = /\s*alignment-baseline\s*:\s*([^;\s]*)\s*/;
          var text = document.querySelectorAll("#t794f466b7c9245139e15937d734b2294 text");
          for(var i = 0; i != text.length; ++i)
          {
            var match = re.exec(text[i].attributes.style.value);
            if(match)
            {
              if(match[1] == "middle")
              {
                var style = getComputedStyle(text[i]);
                var font_size = style.fontSize.substr(0, style.fontSize.length - 2);
                var dy = text[i].dy.baseVal.length ? text[i].dy.baseVal[0].value : 0;
                dy += 0.4 * font_size;
                text[i].setAttribute("dy", dy);
              }
            }
          }
        }
        if(!window.CSS.supports("baseline-shift", "0"))
        {
          var re = /\s*baseline-shift\s*:\s*([^;\s]*)\s*/;
          var text = document.querySelectorAll("#t794f466b7c9245139e15937d734b2294 text");
          for(var i = 0; i != text.length; ++i)
          {
            var match = re.exec(text[i].attributes.style.value);
            if(match)
            {
              var style = getComputedStyle(text[i]);
              var font_size = style.fontSize.substr(0, style.fontSize.length - 2);
              var percent = 0.01 * match[1].substr(0, match[1].length-1);
              var dy = text[i].dy.baseVal.length ? text[i].dy.baseVal[0].value : 0;
              dy -= percent * font_size
              text[i].setAttribute("dy", dy);
            }
          }
        }
      }
    })();
    </script><script>
    (function()
    {
      var data_tables = [{"data": [[0.0, 0.02040816326530612, 0.04081632653061224, 0.061224489795918366, 0.08163265306122448, 0.1020408163265306, 0.12244897959183673, 0.14285714285714285, 0.16326530612244897, 0.18367346938775508, 0.2040816326530612, 0.22448979591836732, 0.24489795918367346, 0.26530612244897955, 0.2857142857142857, 0.3061224489795918, 0.32653061224489793, 0.3469387755102041, 0.36734693877551017, 0.3877551020408163, 0.4081632653061224, 0.42857142857142855, 0.44897959183673464, 0.4693877551020408, 0.4897959183673469, 0.5102040816326531, 0.5306122448979591, 0.5510204081632653, 0.5714285714285714, 0.5918367346938775, 0.6122448979591836, 0.6326530612244897, 0.6530612244897959, 0.673469387755102, 0.6938775510204082, 0.7142857142857142, 0.7346938775510203, 0.7551020408163265, 0.7755102040816326, 0.7959183673469387, 0.8163265306122448, 0.836734693877551, 0.8571428571428571, 0.8775510204081632, 0.8979591836734693, 0.9183673469387754, 0.9387755102040816, 0.9591836734693877, 0.9795918367346939, 1.0], [0.0, 0.00041649312786339016, 0.0016659725114535606, 0.003748438150770512, 0.006663890045814243, 0.010412328196584754, 0.014993752603082049, 0.02040816326530612, 0.02665556018325697, 0.033735943356934604, 0.041649312786339016, 0.05039566847147021, 0.059975010412328195, 0.07038733860891293, 0.08163265306122448, 0.09371095376926278, 0.10662224073302788, 0.12036651395251978, 0.13494377342773842, 0.15035401915868388, 0.16659725114535606, 0.18367346938775508, 0.20158267388588083, 0.22032486463973341, 0.23990004164931278, 0.2603082049146189, 0.2815493544356517, 0.3036234902124114, 0.32653061224489793, 0.3502707205331112, 0.3748438150770511, 0.40024989587671794, 0.4264889629321115, 0.453561016243232, 0.4814660558100791, 0.510204081632653, 0.5397750937109537, 0.5701790920449812, 0.6014160766347355, 0.6334860474802164, 0.6663890045814242, 0.7001249479383589, 0.7346938775510203, 0.7700957934194085, 0.8063306955435233, 0.8433985839233651, 0.8812994585589337, 0.920033319450229, 0.9596001665972511, 1.0]], "title": "Plot Data", "names": ["x", "y0"], "id": "tad1f8a1c0bab48f4a1c60839146c3f6c", "filename": "toyplot"}];
    
      function save_csv(data_table)
      {
        var uri = "data:text/csv;charset=utf-8,";
        uri += data_table.names.join(",") + "\n";
        for(var i = 0; i != data_table.data[0].length; ++i)
        {
          for(var j = 0; j != data_table.data.length; ++j)
          {
            if(j)
              uri += ",";
            uri += data_table.data[j][i];
          }
          uri += "\n";
        }
        uri = encodeURI(uri);
    
        var link = document.createElement("a");
        if(typeof link.download != "undefined")
        {
          link.href = uri;
          link.style = "visibility:hidden";
          link.download = data_table.filename + ".csv";
    
          document.body.appendChild(link);
          link.click();
          document.body.removeChild(link);
        }
        else
        {
          window.open(uri);
        }
      }
    
      function open_popup(data_table)
      {
        return function(e)
        {
          var popup = document.querySelector("#t794f466b7c9245139e15937d734b2294 .toyplot-mark-popup");
          popup.querySelector(".toyplot-mark-popup-title").innerHTML = data_table.title;
          popup.querySelector(".toyplot-mark-popup-save-csv").onclick = function() { popup.style.visibility = "hidden"; save_csv(data_table); }
          popup.style.left = (e.clientX - 50) + "px";
          popup.style.top = (e.clientY - 20) + "px";
          popup.style.visibility = "visible";
          e.stopPropagation();
          e.preventDefault();
        }
    
      }
    
      for(var i = 0; i != data_tables.length; ++i)
      {
        var data_table = data_tables[i];
        var event_target = document.querySelector("#" + data_table.id);
        event_target.oncontextmenu = open_popup(data_table);
      }
    })();
    </script><script>
    (function()
    {
      var axes = {"t6d296b08f9a84104a55fa2d499c320ae": {"x": [{"domain": {"bounds": {"max": Infinity, "min": -Infinity}, "max": 1.0, "min": 0.0}, "range": {"bounds": {"max": Infinity, "min": -Infinity}, "max": 240.0, "min": 60.0}, "scale": "linear"}], "y": [{"domain": {"bounds": {"max": Infinity, "min": -Infinity}, "max": 1.0, "min": 0.0}, "range": {"bounds": {"max": -Infinity, "min": Infinity}, "max": 60.0, "min": 240.0}, "scale": "linear"}]}};
    
      function sign(x)
      {
        return x < 0 ? -1 : x > 0 ? 1 : 0;
      }
    
      function _mix(a, b, amount)
      {
        return ((1.0 - amount) * a) + (amount * b);
      }
    
      function _log(x, base)
      {
        return Math.log(Math.abs(x)) / Math.log(base);
      }
    
      function _in_range(a, x, b)
      {
        var left = Math.min(a, b);
        var right = Math.max(a, b);
        return left <= x && x <= right;
      }
    
      function to_domain(projection, range)
      {
        for(var i = 0; i != projection.length; ++i)
        {
          var segment = projection[i];
          if(_in_range(segment.range.bounds.min, range, segment.range.bounds.max))
          {
            if(segment.scale == "linear")
            {
              var amount = (range - segment.range.min) / (segment.range.max - segment.range.min);
              return _mix(segment.domain.min, segment.domain.max, amount)
            }
            else if(segment.scale[0] == "log")
            {
              var amount = (range - segment.range.min) / (segment.range.max - segment.range.min);
              var base = segment.scale[1];
              return sign(segment.domain.min) * Math.pow(base, _mix(_log(segment.domain.min, base), _log(segment.domain.max, base), amount));
            }
          }
        }
      }
    
      // Compute mouse coordinates relative to a DOM object, with thanks to d3js.org, where this code originated.
      function d3_mousePoint(container, e)
      {
        if (e.changedTouches) e = e.changedTouches[0];
        var svg = container.ownerSVGElement || container;
        if (svg.createSVGPoint) {
          var point = svg.createSVGPoint();
          point.x = e.clientX, point.y = e.clientY;
          point = point.matrixTransform(container.getScreenCTM().inverse());
          return [point.x, point.y];
        }
        var rect = container.getBoundingClientRect();
        return [e.clientX - rect.left - container.clientLeft, e.clientY - rect.top - container.clientTop];
      };
    
      function display_coordinates(e)
      {
        var dom_axes = e.currentTarget.parentElement;
        var data = axes[dom_axes.id];
    
        point = d3_mousePoint(e.target, e);
        var x = Number(to_domain(data["x"], point[0])).toFixed(2);
        var y = Number(to_domain(data["y"], point[1])).toFixed(2);
    
        var coordinates = dom_axes.querySelectorAll(".toyplot-coordinates");
        for(var i = 0; i != coordinates.length; ++i)
        {
          coordinates[i].style.visibility = "visible";
          coordinates[i].querySelector("text").textContent = "x=" + x + " y=" + y;
        }
      }
    
      function clear_coordinates(e)
      {
        var dom_axes = e.currentTarget.parentElement;
        var coordinates = dom_axes.querySelectorAll(".toyplot-coordinates");
        for(var i = 0; i != coordinates.length; ++i)
          coordinates[i].style.visibility = "hidden";
      }
    
      for(var axes_id in axes)
      {
        var event_target = document.querySelector("#" + axes_id + " .toyplot-coordinate-events");
        event_target.onmousemove = display_coordinates;
        event_target.onmouseout = clear_coordinates;
      }
    })();
    </script></div></div>


Note that no special import statements, magics, backends, or
configuration is required - Toyplot Just Works. In this case,
autorendering is enabled by default when you create a new canvas.
Toyplot knows that it's being run in the Jupyter notebook environment,
and when you execute a notebook cell that contains a canvas with
autorendering enabled, it inserts the rendered canvas in the cell
output. Note that this is not the same as Jupyter's rich output system -
a Toyplot canvas doesn't have to be the result of an expression to be
rendered, and you can create multiple Toyplot canvases in a single
notebook cell (handy when producing multiple figures in a loop), and
they will all be rendered.

Autorendering for a canvas is automatically disabled if you pass it to a
rendering backend or a display. So while the above example automatically
rendered the canvas into a notebook cell, the following will not:

.. code:: python

    canvas = toyplot.Canvas(width=300)
    canvas.axes().plot(x, y)
    toyplot.pdf.render(canvas, "figure2.pdf")

In some circumstances you may want to disable autorendering yourself,
which you can do when the canvas is created:

.. code:: python

    canvas = toyplot.Canvas(width=300, autorender=False)
    canvas.axes().plot(x, y);
