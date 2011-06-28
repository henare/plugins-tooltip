jQuery tooltip plugin
=====================

This is a simple tooltip plugin that takes the **title** attribute of an element and replaces it with a DOM node that allows you to style it any way you like. I have included three options to generate the tooltip content.

1. A string value which is the content of the tooltip. This can include any html elements you would like.
2. A selector for a document element. The tooltip will then look for that element and insert its contents into the tooltip. The setting **domNode: true** will activate this.
3. AJAX content into the tooltip by setting **ajax: true** and putting the URL of the ajax document in the title attribute.

Other settings for the plugin are as follows:

* **toolID** - set the ID of the tooltip so that can have different tooltip styles on the same page. The default ID of the tooltip is “tooltip”.
* **offsetY** - the vertical offset of the tooltip relative to its initial positioning.
* **offsetX** - the horizontal offset of the tooltip relative to its initial positioning.
* **staticTool** - allows the tooltip to be statically positioned relative the DOM element. The default: false will let the tooltip follow the mouse around whilst it is over the element.
* **staticPos** - sets the positioning of the tooltip in relation to the associated element. Available positions are: ‘top’, bottom’, ‘left’, ‘right’.

To call the tooltip just add the method tooltip() to your selector and pass the options you want in the document ready function, and call the javascript thus:

    $(document).ready(function(){
        $('#myElement').tooltip({
          staticTool : true,
          staticPos : 'top',
          offsetY : -10,
          offsetX : 10
        });
    });

Here is what the HTML might look like:

    <div id='myElement' title='<p>the content of the tooltip</p>'>
        <p>A box with a tooltip on it</p>
    </div>

Check out the [demo page](http://dansdom.github.com/plugins-tooltip/). Happy tooltipping everybody!
