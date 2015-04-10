
  .. image:: ../artwork/toyplot.png
    :width: 200px
    :align: right
  
.. _units:

Units
-----

There are several places in Toyplot where you will need to specify
quantities with real-world units, including canvas dimensions, font
sizes, and target dimensions for document-oriented backends such as
:mod:`toyplot.eps` and :mod:`toyplot.pdf`. For example, when
creating a canvas, explicitly or implicitly through the convenience API,
you could specify its width and height in inches:

.. code:: python

    import numpy
    x = numpy.linspace(0, 1)
    y = x ** 2
.. code:: python

    import toyplot
    toyplot.plot(x, y, width="3in", height="2in");


.. raw:: html

    <div align="center" class="toyplot" id="taba44c0148e247d1b88532e9a8be1e7b"><svg height="192.0px" id="t4d7d6180a5d74200b1bca172dfbd5d8e" style="background-color:transparent;fill:#292724;fill-opacity:1.0;font-family:helvetica;font-size:12px;opacity:1.0;stroke:#292724;stroke-opacity:1.0;stroke-width:1.0" width="288.0px" xmlns="http://www.w3.org/2000/svg" xmlns:toyplot="http://www.sandia.gov/toyplot"><g class="toyplot-axes-Cartesian" id="t1a63dadfd59944368829f60e8e2bffc2"><toyplot:axes>{"x": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 228.0, "min": 60}, "scale": "linear"}], "y": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 132.0, "min": 60}, "scale": "linear"}]}</toyplot:axes><clipPath id="td7592f58df0c4f1b9b90bec018c98e87"><rect height="92.0" width="188.0" x="50" y="50"></rect></clipPath><g class="toyplot-coordinate-events" clip-path="url(#td7592f58df0c4f1b9b90bec018c98e87)" style="cursor:crosshair"><rect height="92.0" style="pointer-events:all;visibility:hidden" width="188.0" x="50" y="50"></rect><g class="toyplot-mark-Plot" id="td7dacd7c23814ee8b6af07b6d884f2de" style="fill:none"><toyplot:data-table title="Plot Data">{"data": [[0.0, 0.02040816326530612, 0.04081632653061224, 0.061224489795918366, 0.08163265306122448, 0.1020408163265306, 0.12244897959183673, 0.14285714285714285, 0.16326530612244897, 0.18367346938775508, 0.2040816326530612, 0.22448979591836732, 0.24489795918367346, 0.26530612244897955, 0.2857142857142857, 0.3061224489795918, 0.32653061224489793, 0.3469387755102041, 0.36734693877551017, 0.3877551020408163, 0.4081632653061224, 0.42857142857142855, 0.44897959183673464, 0.4693877551020408, 0.4897959183673469, 0.5102040816326531, 0.5306122448979591, 0.5510204081632653, 0.5714285714285714, 0.5918367346938775, 0.6122448979591836, 0.6326530612244897, 0.6530612244897959, 0.673469387755102, 0.6938775510204082, 0.7142857142857142, 0.7346938775510203, 0.7551020408163265, 0.7755102040816326, 0.7959183673469387, 0.8163265306122448, 0.836734693877551, 0.8571428571428571, 0.8775510204081632, 0.8979591836734693, 0.9183673469387754, 0.9387755102040816, 0.9591836734693877, 0.9795918367346939, 1.0], [0.0, 0.00041649312786339016, 0.0016659725114535606, 0.003748438150770512, 0.006663890045814243, 0.010412328196584754, 0.014993752603082049, 0.02040816326530612, 0.02665556018325697, 0.033735943356934604, 0.041649312786339016, 0.05039566847147021, 0.059975010412328195, 0.07038733860891293, 0.08163265306122448, 0.09371095376926278, 0.10662224073302788, 0.12036651395251978, 0.13494377342773842, 0.15035401915868388, 0.16659725114535606, 0.18367346938775508, 0.20158267388588083, 0.22032486463973341, 0.23990004164931278, 0.2603082049146189, 0.2815493544356517, 0.3036234902124114, 0.32653061224489793, 0.3502707205331112, 0.3748438150770511, 0.40024989587671794, 0.4264889629321115, 0.453561016243232, 0.4814660558100791, 0.510204081632653, 0.5397750937109537, 0.5701790920449812, 0.6014160766347355, 0.6334860474802164, 0.6663890045814242, 0.7001249479383589, 0.7346938775510203, 0.7700957934194085, 0.8063306955435233, 0.8433985839233651, 0.8812994585589337, 0.920033319450229, 0.9596001665972511, 1.0], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0]], "names": ["x", "y0", "marker0", "size0", "fill0:red", "fill0:green", "fill0:blue", "fill0:alpha", "stroke0:red", "stroke0:green", "stroke0:blue", "stroke0:alpha", "opacity0"]}</toyplot:data-table><g class="toyplot-Series"><path d="M 60.0 132.0 L 63.428571428571431 131.97001249479382 L 66.857142857142861 131.88004997917534 L 70.285714285714278 131.73011245314453 L 73.714285714285708 131.52019991670136 L 77.142857142857139 131.25031236984591 L 80.571428571428569 130.92044981257811 L 84.0 130.53061224489795 L 87.428571428571431 130.08079966680549 L 90.857142857142861 129.57101207830073 L 94.285714285714278 129.0012494793836 L 97.714285714285708 128.37151187005412 L 101.14285714285714 127.68179925031237 L 104.57142857142856 126.93211162015827 L 108.0 126.12244897959184 L 111.42857142857142 125.25281132861308 L 114.85714285714286 124.323198667222 L 118.28571428571428 123.33361099541858 L 121.71428571428571 122.28404831320283 L 125.14285714285714 121.17451062057476 L 128.57142857142856 120.00499791753435 L 132.0 118.77551020408163 L 135.42857142857142 117.48604748021658 L 138.85714285714283 116.13660974593918 L 142.28571428571428 114.72719700124948 L 145.71428571428572 113.25780924614745 L 149.14285714285711 111.72844648063307 L 152.57142857142856 110.13910870470639 L 156.0 108.48979591836735 L 159.42857142857144 106.78050812161598 L 162.85714285714283 105.01124531445231 L 166.28571428571428 103.18200749687631 L 169.71428571428572 101.29279466888796 L 173.14285714285714 99.343606830487289 L 176.57142857142856 97.334443981674298 L 180.0 95.26530612244899 L 183.42857142857142 93.136193252811339 L 186.85714285714283 90.947105372761357 L 190.28571428571428 88.698042482299044 L 193.71428571428569 86.389004581424416 L 197.14285714285714 84.019991670137458 L 200.57142857142856 81.591003748438169 L 204.0 79.102040816326536 L 207.42857142857142 76.553102873802587 L 210.85714285714283 73.944189920866322 L 214.28571428571428 71.275301957517712 L 217.71428571428569 68.546438983756772 L 221.14285714285714 65.757600999583502 L 224.57142857142856 62.908788004997916 L 228.0 60.0" style="fill:none;stroke:rgba(40%,76.1%,64.7%,1);stroke-opacity:1.0;stroke-width:2.0"></path></g></g></g><g class="toyplot-coordinates" style="visibility:hidden"><rect height="14" style="fill:white;opacity:0.75;stroke:none" width="90.0" x="138.0" y="60"></rect><text style="alignment-baseline:middle;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="183.0" y="67.0"></text></g><line style="" x1="60.0" x2="228.0" y1="142.0" y2="142.0"></line><g><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="60.0" y="142.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="144.0" y="142.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="228.0" y="142.0">1.0</text></g><line style="" x1="50" x2="50" y1="60.0" y2="132.0"></line><g><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 132.0)" x="50" y="132.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 96.0)" x="50" y="96.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 60.0)" x="50" y="60.0">1.0</text></g></g></svg><div class="toyplot-controls"><ul class="toyplot-mark-popup" onmouseleave="this.style.visibility='hidden'" style="background:rgba(0%,0%,0%,0.75);border:0;border-radius:6px;color:white;cursor:default;list-style:none;margin:0;padding:5px;position:fixed;visibility:hidden"><li class="toyplot-mark-popup-title" style="color:lightgray;cursor:default;padding:5px;list-style:none;margin:0;"></li><li class="toyplot-mark-popup-save-csv" onmouseout="this.style.color='white';this.style.background='steelblue'" onmouseover="this.style.color='steelblue';this.style.background='white'" style="border-radius:3px;padding:5px;list-style:none;margin:0;">Save as .csv</li></ul><script>
        (function()
        {
          // Workaround for browsers that don't support alignment-baseline
          if(window.CSS !== undefined && window.CSS.supports !== undefined)
          {
            if(!window.CSS.supports("alignment-baseline", "middle"))
            {
              var re = /\s*alignment-baseline\s*:\s*([^;\s]*)\s*/;
              var text = document.querySelectorAll("#taba44c0148e247d1b88532e9a8be1e7b text");
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
              var text = document.querySelectorAll("#taba44c0148e247d1b88532e9a8be1e7b text");
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
        // Allow users to extract embedded raw data
        (function()
        {
          var root_id="taba44c0148e247d1b88532e9a8be1e7b";
    
          function save_csv(dataset)
          {
            uri = "data:text/csv;charset=utf-8,";
            data = JSON.parse(dataset.textContent);
            uri += data.names.join(",") + "\n";
            for(var i = 0; i != data.data[0].length; ++i)
            {
              for(var j = 0; j != data.data.length; ++j)
              {
                if(j)
                  uri += ",";
                uri += data.data[j][i];
              }
              uri += "\n";
            }
    
            uri = encodeURI(uri);
            window.open(uri);
          }
    
          function open_popup(dataset)
          {
            return function(e)
            {
              var popup = document.querySelector("#" + root_id + " .toyplot-mark-popup");
              popup.querySelector(".toyplot-mark-popup-title").innerHTML = dataset.getAttribute("title");
              popup.querySelector(".toyplot-mark-popup-save-csv").onclick = function() { popup.style.visibility = "hidden"; save_csv(dataset); }
              popup.style.left = (e.clientX - 50) + "px";
              popup.style.top = (e.clientY - 20) + "px";
              popup.style.visibility = "visible";
              e.stopPropagation();
              e.preventDefault();
            }
    
          }
    
          var datasets = document.querySelectorAll("#" + root_id + " toyplot\\:data-table");
          for(var i = 0; i != datasets.length; ++i)
          {
            var dataset = datasets[i];
            var mark = dataset.parentElement;
            mark.oncontextmenu = open_popup(dataset);
          }
        })();
        </script><script>
        (function()
        {
          var root_id="taba44c0148e247d1b88532e9a8be1e7b";
    
          function sign(x)
          {
            if(x < 0)
              return -1;
            if(x > 0)
              return 1;
            return 0;
          }
    
          function log_n(x, base)
          {
            return Math.log(x) / Math.log(base);
          }
    
          function mix(a, b, amount)
          {
            return ((1.0 - amount) * a) + (amount * b);
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
            var x = null;
            var y = null;
    
            var axes = e.currentTarget.parentElement;
            var data = JSON.parse(axes.querySelector("toyplot\\:axes").textContent);
    
            point = d3_mousePoint(e.target, e);
    
            for(var i = 0; i != data["x"].length; ++i)
            {
              var segment = data["x"][i];
              if(segment.range.min <= point[0] && point[0] < segment.range.max)
              {
                var normalized = (point[0] - segment.range.min) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  x = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  x = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            for(var i = 0; i != data["y"].length; ++i)
            {
              var segment = data["y"][i];
              if(segment.range.min <= point[1] && point[1] < segment.range.max)
              {
                var normalized = (segment.range.max - point[1]) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  y = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  y = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            if(x !== null && y !== null)
              text = "x=" + x + " y=" + y;
            else if(x !== null)
              text = "x=" + x;
            else if(y !== null)
              text = "y=" + y;
            else
              text = null;
    
            if(text !== null)
            {
              var coordinates = axes.querySelectorAll(".toyplot-coordinates");
              for(var i = 0; i != coordinates.length; ++i)
              {
                coordinates[i].style.visibility = "visible";
                coordinates[i].querySelector("text").textContent = text;
              }
            }
          }
    
          function clear_coordinates(e)
          {
            var axes = e.currentTarget.parentElement;
            var coordinates = axes.querySelectorAll(".toyplot-coordinates");
            for(var i = 0; i != coordinates.length; ++i)
              coordinates[i].style.visibility = "hidden";
          }
    
          var axes = document.querySelectorAll("#" + root_id + " .toyplot-axes-Cartesian .toyplot-coordinate-events");
          for(var i = 0; i != axes.length; ++i)
          {
            axes[i].onmousemove = display_coordinates;
            axes[i].onmouseout = clear_coordinates;
          }
        })();
        </script></div></div>


You can also specify the quantity and units separately:

.. code:: python

    toyplot.plot(x, y, width=(3, "in"), height=(2, "in"));


.. raw:: html

    <div align="center" class="toyplot" id="tf21633582bd744e69919b4b6f0c6e6b6"><svg height="192.0px" id="t347a4cee58614347bc40e97149dc81af" style="background-color:transparent;fill:#292724;fill-opacity:1.0;font-family:helvetica;font-size:12px;opacity:1.0;stroke:#292724;stroke-opacity:1.0;stroke-width:1.0" width="288.0px" xmlns="http://www.w3.org/2000/svg" xmlns:toyplot="http://www.sandia.gov/toyplot"><g class="toyplot-axes-Cartesian" id="t575d856e7ab644aebc5f15bd0a1c2a51"><toyplot:axes>{"x": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 228.0, "min": 60}, "scale": "linear"}], "y": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 132.0, "min": 60}, "scale": "linear"}]}</toyplot:axes><clipPath id="t216247c1bad2416a929bcdc365a43561"><rect height="92.0" width="188.0" x="50" y="50"></rect></clipPath><g class="toyplot-coordinate-events" clip-path="url(#t216247c1bad2416a929bcdc365a43561)" style="cursor:crosshair"><rect height="92.0" style="pointer-events:all;visibility:hidden" width="188.0" x="50" y="50"></rect><g class="toyplot-mark-Plot" id="td2c23e3a9c5948a7891d7d954de67c0d" style="fill:none"><toyplot:data-table title="Plot Data">{"data": [[0.0, 0.02040816326530612, 0.04081632653061224, 0.061224489795918366, 0.08163265306122448, 0.1020408163265306, 0.12244897959183673, 0.14285714285714285, 0.16326530612244897, 0.18367346938775508, 0.2040816326530612, 0.22448979591836732, 0.24489795918367346, 0.26530612244897955, 0.2857142857142857, 0.3061224489795918, 0.32653061224489793, 0.3469387755102041, 0.36734693877551017, 0.3877551020408163, 0.4081632653061224, 0.42857142857142855, 0.44897959183673464, 0.4693877551020408, 0.4897959183673469, 0.5102040816326531, 0.5306122448979591, 0.5510204081632653, 0.5714285714285714, 0.5918367346938775, 0.6122448979591836, 0.6326530612244897, 0.6530612244897959, 0.673469387755102, 0.6938775510204082, 0.7142857142857142, 0.7346938775510203, 0.7551020408163265, 0.7755102040816326, 0.7959183673469387, 0.8163265306122448, 0.836734693877551, 0.8571428571428571, 0.8775510204081632, 0.8979591836734693, 0.9183673469387754, 0.9387755102040816, 0.9591836734693877, 0.9795918367346939, 1.0], [0.0, 0.00041649312786339016, 0.0016659725114535606, 0.003748438150770512, 0.006663890045814243, 0.010412328196584754, 0.014993752603082049, 0.02040816326530612, 0.02665556018325697, 0.033735943356934604, 0.041649312786339016, 0.05039566847147021, 0.059975010412328195, 0.07038733860891293, 0.08163265306122448, 0.09371095376926278, 0.10662224073302788, 0.12036651395251978, 0.13494377342773842, 0.15035401915868388, 0.16659725114535606, 0.18367346938775508, 0.20158267388588083, 0.22032486463973341, 0.23990004164931278, 0.2603082049146189, 0.2815493544356517, 0.3036234902124114, 0.32653061224489793, 0.3502707205331112, 0.3748438150770511, 0.40024989587671794, 0.4264889629321115, 0.453561016243232, 0.4814660558100791, 0.510204081632653, 0.5397750937109537, 0.5701790920449812, 0.6014160766347355, 0.6334860474802164, 0.6663890045814242, 0.7001249479383589, 0.7346938775510203, 0.7700957934194085, 0.8063306955435233, 0.8433985839233651, 0.8812994585589337, 0.920033319450229, 0.9596001665972511, 1.0], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0]], "names": ["x", "y0", "marker0", "size0", "fill0:red", "fill0:green", "fill0:blue", "fill0:alpha", "stroke0:red", "stroke0:green", "stroke0:blue", "stroke0:alpha", "opacity0"]}</toyplot:data-table><g class="toyplot-Series"><path d="M 60.0 132.0 L 63.428571428571431 131.97001249479382 L 66.857142857142861 131.88004997917534 L 70.285714285714278 131.73011245314453 L 73.714285714285708 131.52019991670136 L 77.142857142857139 131.25031236984591 L 80.571428571428569 130.92044981257811 L 84.0 130.53061224489795 L 87.428571428571431 130.08079966680549 L 90.857142857142861 129.57101207830073 L 94.285714285714278 129.0012494793836 L 97.714285714285708 128.37151187005412 L 101.14285714285714 127.68179925031237 L 104.57142857142856 126.93211162015827 L 108.0 126.12244897959184 L 111.42857142857142 125.25281132861308 L 114.85714285714286 124.323198667222 L 118.28571428571428 123.33361099541858 L 121.71428571428571 122.28404831320283 L 125.14285714285714 121.17451062057476 L 128.57142857142856 120.00499791753435 L 132.0 118.77551020408163 L 135.42857142857142 117.48604748021658 L 138.85714285714283 116.13660974593918 L 142.28571428571428 114.72719700124948 L 145.71428571428572 113.25780924614745 L 149.14285714285711 111.72844648063307 L 152.57142857142856 110.13910870470639 L 156.0 108.48979591836735 L 159.42857142857144 106.78050812161598 L 162.85714285714283 105.01124531445231 L 166.28571428571428 103.18200749687631 L 169.71428571428572 101.29279466888796 L 173.14285714285714 99.343606830487289 L 176.57142857142856 97.334443981674298 L 180.0 95.26530612244899 L 183.42857142857142 93.136193252811339 L 186.85714285714283 90.947105372761357 L 190.28571428571428 88.698042482299044 L 193.71428571428569 86.389004581424416 L 197.14285714285714 84.019991670137458 L 200.57142857142856 81.591003748438169 L 204.0 79.102040816326536 L 207.42857142857142 76.553102873802587 L 210.85714285714283 73.944189920866322 L 214.28571428571428 71.275301957517712 L 217.71428571428569 68.546438983756772 L 221.14285714285714 65.757600999583502 L 224.57142857142856 62.908788004997916 L 228.0 60.0" style="fill:none;stroke:rgba(40%,76.1%,64.7%,1);stroke-opacity:1.0;stroke-width:2.0"></path></g></g></g><g class="toyplot-coordinates" style="visibility:hidden"><rect height="14" style="fill:white;opacity:0.75;stroke:none" width="90.0" x="138.0" y="60"></rect><text style="alignment-baseline:middle;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="183.0" y="67.0"></text></g><line style="" x1="60.0" x2="228.0" y1="142.0" y2="142.0"></line><g><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="60.0" y="142.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="144.0" y="142.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="228.0" y="142.0">1.0</text></g><line style="" x1="50" x2="50" y1="60.0" y2="132.0"></line><g><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 132.0)" x="50" y="132.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 96.0)" x="50" y="96.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 60.0)" x="50" y="60.0">1.0</text></g></g></svg><div class="toyplot-controls"><ul class="toyplot-mark-popup" onmouseleave="this.style.visibility='hidden'" style="background:rgba(0%,0%,0%,0.75);border:0;border-radius:6px;color:white;cursor:default;list-style:none;margin:0;padding:5px;position:fixed;visibility:hidden"><li class="toyplot-mark-popup-title" style="color:lightgray;cursor:default;padding:5px;list-style:none;margin:0;"></li><li class="toyplot-mark-popup-save-csv" onmouseout="this.style.color='white';this.style.background='steelblue'" onmouseover="this.style.color='steelblue';this.style.background='white'" style="border-radius:3px;padding:5px;list-style:none;margin:0;">Save as .csv</li></ul><script>
        (function()
        {
          // Workaround for browsers that don't support alignment-baseline
          if(window.CSS !== undefined && window.CSS.supports !== undefined)
          {
            if(!window.CSS.supports("alignment-baseline", "middle"))
            {
              var re = /\s*alignment-baseline\s*:\s*([^;\s]*)\s*/;
              var text = document.querySelectorAll("#tf21633582bd744e69919b4b6f0c6e6b6 text");
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
              var text = document.querySelectorAll("#tf21633582bd744e69919b4b6f0c6e6b6 text");
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
        // Allow users to extract embedded raw data
        (function()
        {
          var root_id="tf21633582bd744e69919b4b6f0c6e6b6";
    
          function save_csv(dataset)
          {
            uri = "data:text/csv;charset=utf-8,";
            data = JSON.parse(dataset.textContent);
            uri += data.names.join(",") + "\n";
            for(var i = 0; i != data.data[0].length; ++i)
            {
              for(var j = 0; j != data.data.length; ++j)
              {
                if(j)
                  uri += ",";
                uri += data.data[j][i];
              }
              uri += "\n";
            }
    
            uri = encodeURI(uri);
            window.open(uri);
          }
    
          function open_popup(dataset)
          {
            return function(e)
            {
              var popup = document.querySelector("#" + root_id + " .toyplot-mark-popup");
              popup.querySelector(".toyplot-mark-popup-title").innerHTML = dataset.getAttribute("title");
              popup.querySelector(".toyplot-mark-popup-save-csv").onclick = function() { popup.style.visibility = "hidden"; save_csv(dataset); }
              popup.style.left = (e.clientX - 50) + "px";
              popup.style.top = (e.clientY - 20) + "px";
              popup.style.visibility = "visible";
              e.stopPropagation();
              e.preventDefault();
            }
    
          }
    
          var datasets = document.querySelectorAll("#" + root_id + " toyplot\\:data-table");
          for(var i = 0; i != datasets.length; ++i)
          {
            var dataset = datasets[i];
            var mark = dataset.parentElement;
            mark.oncontextmenu = open_popup(dataset);
          }
        })();
        </script><script>
        (function()
        {
          var root_id="tf21633582bd744e69919b4b6f0c6e6b6";
    
          function sign(x)
          {
            if(x < 0)
              return -1;
            if(x > 0)
              return 1;
            return 0;
          }
    
          function log_n(x, base)
          {
            return Math.log(x) / Math.log(base);
          }
    
          function mix(a, b, amount)
          {
            return ((1.0 - amount) * a) + (amount * b);
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
            var x = null;
            var y = null;
    
            var axes = e.currentTarget.parentElement;
            var data = JSON.parse(axes.querySelector("toyplot\\:axes").textContent);
    
            point = d3_mousePoint(e.target, e);
    
            for(var i = 0; i != data["x"].length; ++i)
            {
              var segment = data["x"][i];
              if(segment.range.min <= point[0] && point[0] < segment.range.max)
              {
                var normalized = (point[0] - segment.range.min) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  x = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  x = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            for(var i = 0; i != data["y"].length; ++i)
            {
              var segment = data["y"][i];
              if(segment.range.min <= point[1] && point[1] < segment.range.max)
              {
                var normalized = (segment.range.max - point[1]) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  y = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  y = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            if(x !== null && y !== null)
              text = "x=" + x + " y=" + y;
            else if(x !== null)
              text = "x=" + x;
            else if(y !== null)
              text = "y=" + y;
            else
              text = null;
    
            if(text !== null)
            {
              var coordinates = axes.querySelectorAll(".toyplot-coordinates");
              for(var i = 0; i != coordinates.length; ++i)
              {
                coordinates[i].style.visibility = "visible";
                coordinates[i].querySelector("text").textContent = text;
              }
            }
          }
    
          function clear_coordinates(e)
          {
            var axes = e.currentTarget.parentElement;
            var coordinates = axes.querySelectorAll(".toyplot-coordinates");
            for(var i = 0; i != coordinates.length; ++i)
              coordinates[i].style.visibility = "hidden";
          }
    
          var axes = document.querySelectorAll("#" + root_id + " .toyplot-axes-Cartesian .toyplot-coordinate-events");
          for(var i = 0; i != axes.length; ++i)
          {
            axes[i].onmousemove = display_coordinates;
            axes[i].onmouseout = clear_coordinates;
          }
        })();
        </script></div></div>


If you rendered either plot using the EPS or PDF backend, the resulting
document size would match your canvas dimensions.

If you don't specify any units, the canvas assumes a default unit of
"pixels":

.. code:: python

    toyplot.plot(x, y, width=600, height=400);


.. raw:: html

    <div align="center" class="toyplot" id="t4bda4355f4884e24abd67630d75dd277"><svg height="400.0px" id="tf6fee17d91a64783b33a984b0f7ed938" style="background-color:transparent;fill:#292724;fill-opacity:1.0;font-family:helvetica;font-size:12px;opacity:1.0;stroke:#292724;stroke-opacity:1.0;stroke-width:1.0" width="600.0px" xmlns="http://www.w3.org/2000/svg" xmlns:toyplot="http://www.sandia.gov/toyplot"><g class="toyplot-axes-Cartesian" id="t2e1b0ede11a94e6687ee1e7a6aea53d2"><toyplot:axes>{"x": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 540.0, "min": 60}, "scale": "linear"}], "y": [{"domain": {"max": 1.0, "min": 0.0}, "range": {"max": 340.0, "min": 60}, "scale": "linear"}]}</toyplot:axes><clipPath id="t73d043229aba461e83826a0ff2689fe8"><rect height="300.0" width="500.0" x="50" y="50"></rect></clipPath><g class="toyplot-coordinate-events" clip-path="url(#t73d043229aba461e83826a0ff2689fe8)" style="cursor:crosshair"><rect height="300.0" style="pointer-events:all;visibility:hidden" width="500.0" x="50" y="50"></rect><g class="toyplot-mark-Plot" id="tc01c6621fd8c418b94f9067b1413cf50" style="fill:none"><toyplot:data-table title="Plot Data">{"data": [[0.0, 0.02040816326530612, 0.04081632653061224, 0.061224489795918366, 0.08163265306122448, 0.1020408163265306, 0.12244897959183673, 0.14285714285714285, 0.16326530612244897, 0.18367346938775508, 0.2040816326530612, 0.22448979591836732, 0.24489795918367346, 0.26530612244897955, 0.2857142857142857, 0.3061224489795918, 0.32653061224489793, 0.3469387755102041, 0.36734693877551017, 0.3877551020408163, 0.4081632653061224, 0.42857142857142855, 0.44897959183673464, 0.4693877551020408, 0.4897959183673469, 0.5102040816326531, 0.5306122448979591, 0.5510204081632653, 0.5714285714285714, 0.5918367346938775, 0.6122448979591836, 0.6326530612244897, 0.6530612244897959, 0.673469387755102, 0.6938775510204082, 0.7142857142857142, 0.7346938775510203, 0.7551020408163265, 0.7755102040816326, 0.7959183673469387, 0.8163265306122448, 0.836734693877551, 0.8571428571428571, 0.8775510204081632, 0.8979591836734693, 0.9183673469387754, 0.9387755102040816, 0.9591836734693877, 0.9795918367346939, 1.0], [0.0, 0.00041649312786339016, 0.0016659725114535606, 0.003748438150770512, 0.006663890045814243, 0.010412328196584754, 0.014993752603082049, 0.02040816326530612, 0.02665556018325697, 0.033735943356934604, 0.041649312786339016, 0.05039566847147021, 0.059975010412328195, 0.07038733860891293, 0.08163265306122448, 0.09371095376926278, 0.10662224073302788, 0.12036651395251978, 0.13494377342773842, 0.15035401915868388, 0.16659725114535606, 0.18367346938775508, 0.20158267388588083, 0.22032486463973341, 0.23990004164931278, 0.2603082049146189, 0.2815493544356517, 0.3036234902124114, 0.32653061224489793, 0.3502707205331112, 0.3748438150770511, 0.40024989587671794, 0.4264889629321115, 0.453561016243232, 0.4814660558100791, 0.510204081632653, 0.5397750937109537, 0.5701790920449812, 0.6014160766347355, 0.6334860474802164, 0.6663890045814242, 0.7001249479383589, 0.7346938775510203, 0.7700957934194085, 0.8063306955435233, 0.8433985839233651, 0.8812994585589337, 0.920033319450229, 0.9596001665972511, 1.0], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0, 20.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4, 0.4], [0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902, 0.7607843137254902], [0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118, 0.6470588235294118], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0]], "names": ["x", "y0", "marker0", "size0", "fill0:red", "fill0:green", "fill0:blue", "fill0:alpha", "stroke0:red", "stroke0:green", "stroke0:blue", "stroke0:alpha", "opacity0"]}</toyplot:data-table><g class="toyplot-Series"><path d="M 60.0 340.0 L 69.795918367346943 339.88338192419826 L 79.591836734693871 339.53352769679304 L 89.387755102040813 338.95043731778424 L 99.183673469387742 338.13411078717201 L 108.9795918367347 337.08454810495624 L 118.77551020408163 335.80174927113706 L 128.57142857142856 334.28571428571428 L 138.36734693877548 332.53644314868802 L 148.16326530612244 330.55393586005829 L 157.9591836734694 328.33819241982508 L 167.75510204081633 325.88921282798833 L 177.55102040816325 323.20699708454811 L 187.34693877551018 320.2915451895044 L 197.14285714285714 317.14285714285717 L 206.93877551020407 313.76093294460645 L 216.734693877551 310.1457725947522 L 226.53061224489795 306.29737609329447 L 236.32653061224488 302.21574344023327 L 246.12244897959184 297.90087463556853 L 255.91836734693877 293.35276967930031 L 265.71428571428567 288.57142857142856 L 275.51020408163265 283.55685131195338 L 285.30612244897958 278.30903790087461 L 295.10204081632651 272.82798833819243 L 304.89795918367349 267.1137026239067 L 314.69387755102036 261.1661807580175 L 324.48979591836735 254.9854227405248 L 334.28571428571428 248.57142857142858 L 344.08163265306121 241.92419825072884 L 353.87755102040813 235.04373177842569 L 363.67346938775506 227.93002915451896 L 373.46938775510199 220.58309037900875 L 383.26530612244898 213.00291545189503 L 393.0612244897959 205.18950437317784 L 402.85714285714283 197.14285714285717 L 412.65306122448976 188.86297376093296 L 422.44897959183669 180.34985422740527 L 432.24489795918367 171.60349854227405 L 442.04081632653055 162.62390670553941 L 451.83673469387753 153.41107871720121 L 461.63265306122446 143.96501457725952 L 471.42857142857139 134.28571428571431 L 481.22448979591837 124.37317784256562 L 491.02040816326524 114.22740524781346 L 500.81632653061217 103.84839650145778 L 510.61224489795916 93.23615160349857 L 520.40816326530603 82.390670553935877 L 530.20408163265301 71.311953352769692 L 540.0 60.0" style="fill:none;stroke:rgba(40%,76.1%,64.7%,1);stroke-opacity:1.0;stroke-width:2.0"></path></g></g></g><g class="toyplot-coordinates" style="visibility:hidden"><rect height="14" style="fill:white;opacity:0.75;stroke:none" width="90.0" x="450.0" y="60"></rect><text style="alignment-baseline:middle;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="495.0" y="67.0"></text></g><line style="" x1="60.0" x2="540.0" y1="350.0" y2="350.0"></line><g><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="60.0" y="350.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="300.0" y="350.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:-80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" x="540.0" y="350.0">1.0</text></g><line style="" x1="50" x2="50" y1="60.0" y2="340.0"></line><g><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 340.0)" x="50" y="340.0">0.0</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 200.0)" x="50" y="200.0">0.5</text><text style="alignment-baseline:middle;baseline-shift:80%;font-size:10px;font-weight:normal;stroke:none;text-anchor:middle" transform="rotate(-90, 50, 60.0)" x="50" y="60.0">1.0</text></g></g></svg><div class="toyplot-controls"><ul class="toyplot-mark-popup" onmouseleave="this.style.visibility='hidden'" style="background:rgba(0%,0%,0%,0.75);border:0;border-radius:6px;color:white;cursor:default;list-style:none;margin:0;padding:5px;position:fixed;visibility:hidden"><li class="toyplot-mark-popup-title" style="color:lightgray;cursor:default;padding:5px;list-style:none;margin:0;"></li><li class="toyplot-mark-popup-save-csv" onmouseout="this.style.color='white';this.style.background='steelblue'" onmouseover="this.style.color='steelblue';this.style.background='white'" style="border-radius:3px;padding:5px;list-style:none;margin:0;">Save as .csv</li></ul><script>
        (function()
        {
          // Workaround for browsers that don't support alignment-baseline
          if(window.CSS !== undefined && window.CSS.supports !== undefined)
          {
            if(!window.CSS.supports("alignment-baseline", "middle"))
            {
              var re = /\s*alignment-baseline\s*:\s*([^;\s]*)\s*/;
              var text = document.querySelectorAll("#t4bda4355f4884e24abd67630d75dd277 text");
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
              var text = document.querySelectorAll("#t4bda4355f4884e24abd67630d75dd277 text");
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
        // Allow users to extract embedded raw data
        (function()
        {
          var root_id="t4bda4355f4884e24abd67630d75dd277";
    
          function save_csv(dataset)
          {
            uri = "data:text/csv;charset=utf-8,";
            data = JSON.parse(dataset.textContent);
            uri += data.names.join(",") + "\n";
            for(var i = 0; i != data.data[0].length; ++i)
            {
              for(var j = 0; j != data.data.length; ++j)
              {
                if(j)
                  uri += ",";
                uri += data.data[j][i];
              }
              uri += "\n";
            }
    
            uri = encodeURI(uri);
            window.open(uri);
          }
    
          function open_popup(dataset)
          {
            return function(e)
            {
              var popup = document.querySelector("#" + root_id + " .toyplot-mark-popup");
              popup.querySelector(".toyplot-mark-popup-title").innerHTML = dataset.getAttribute("title");
              popup.querySelector(".toyplot-mark-popup-save-csv").onclick = function() { popup.style.visibility = "hidden"; save_csv(dataset); }
              popup.style.left = (e.clientX - 50) + "px";
              popup.style.top = (e.clientY - 20) + "px";
              popup.style.visibility = "visible";
              e.stopPropagation();
              e.preventDefault();
            }
    
          }
    
          var datasets = document.querySelectorAll("#" + root_id + " toyplot\\:data-table");
          for(var i = 0; i != datasets.length; ++i)
          {
            var dataset = datasets[i];
            var mark = dataset.parentElement;
            mark.oncontextmenu = open_popup(dataset);
          }
        })();
        </script><script>
        (function()
        {
          var root_id="t4bda4355f4884e24abd67630d75dd277";
    
          function sign(x)
          {
            if(x < 0)
              return -1;
            if(x > 0)
              return 1;
            return 0;
          }
    
          function log_n(x, base)
          {
            return Math.log(x) / Math.log(base);
          }
    
          function mix(a, b, amount)
          {
            return ((1.0 - amount) * a) + (amount * b);
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
            var x = null;
            var y = null;
    
            var axes = e.currentTarget.parentElement;
            var data = JSON.parse(axes.querySelector("toyplot\\:axes").textContent);
    
            point = d3_mousePoint(e.target, e);
    
            for(var i = 0; i != data["x"].length; ++i)
            {
              var segment = data["x"][i];
              if(segment.range.min <= point[0] && point[0] < segment.range.max)
              {
                var normalized = (point[0] - segment.range.min) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  x = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  x = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            for(var i = 0; i != data["y"].length; ++i)
            {
              var segment = data["y"][i];
              if(segment.range.min <= point[1] && point[1] < segment.range.max)
              {
                var normalized = (segment.range.max - point[1]) / (segment.range.max - segment.range.min);
                if(segment.scale == "linear")
                {
                  y = Number(mix(segment.domain.min, segment.domain.max, normalized)).toFixed(2);
                }
                else if(segment.scale == "log")
                {
                  y = Number(sign(segment.domain.min) * Math.pow(segment.base, mix(log_n(Math.abs(segment.domain.min), segment.base), log_n(Math.abs(segment.domain.max), segment.base), normalized))).toFixed(2);
                }
              }
            }
    
            if(x !== null && y !== null)
              text = "x=" + x + " y=" + y;
            else if(x !== null)
              text = "x=" + x;
            else if(y !== null)
              text = "y=" + y;
            else
              text = null;
    
            if(text !== null)
            {
              var coordinates = axes.querySelectorAll(".toyplot-coordinates");
              for(var i = 0; i != coordinates.length; ++i)
              {
                coordinates[i].style.visibility = "visible";
                coordinates[i].querySelector("text").textContent = text;
              }
            }
          }
    
          function clear_coordinates(e)
          {
            var axes = e.currentTarget.parentElement;
            var coordinates = axes.querySelectorAll(".toyplot-coordinates");
            for(var i = 0; i != coordinates.length; ++i)
              coordinates[i].style.visibility = "hidden";
          }
    
          var axes = document.querySelectorAll("#" + root_id + " .toyplot-axes-Cartesian .toyplot-coordinate-events");
          for(var i = 0; i != axes.length; ++i)
          {
            axes[i].onmousemove = display_coordinates;
            axes[i].onmouseout = clear_coordinates;
          }
        })();
        </script></div></div>


Note: You're probably used to treating pixels as dimensionless; however
in Toyplot, the "pixels" unit refers to ``CSS pixels``, which are always
1/96th of an inch. Thus, the above example would produce a 6.25 inch
wide PDF or EPS document.

If you rendered the same canvas using the PNG, MP4, or WebM backends, it
would produce 600x400 images / movies by default. Put another way, the
backends that produce raster images always assume 96 DPI, unless
overridden by the caller.

Allowed Units
~~~~~~~~~~~~~

The units and abbreviations currently understood by Toyplot are as
follows:

-  centimeters - "cm", "centimeter", "centimeters"
-  decimeters - "dm", "decimeter", "decimeters"
-  inches - "in", "inch", "inches"
-  meters - "m", "meter", "meters"
-  millimeters - "mm", "millimeter", "millimeters"
-  picas (1/6th of an inch) - "pc", "pica", "picas"
-  pixels (1/96th of an inch) - "px", "pixel", "pixels"
-  points (1/72nd of an inch) - "pt", "point", "points"

Functions that accept quantities with units as parameters will always
accept them in either of two forms:

-  A string that combines the value and unit abbreviations: "5in",
   "12px", "25.4mm".
-  A 2-tuple containing a number and string unit abbreviation: (5,
   "in"), (12, "px"), (25.4, "mm").

Some functions will also accept a single numeric value, with a
documented default unit of measure.

Style Units
~~~~~~~~~~~

Toyplot style parameters always explicitly follow the CSS standard. As
such, they support a subset of unit abbreviations including "cm", "in",
"mm", "pc", "px", and "pt". Although CSS provides additional units for
relative dimensions, they are not recommended for use with Toyplot.