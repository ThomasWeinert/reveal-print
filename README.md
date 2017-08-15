# reveal-print

Extended print trigger for reveal.js

This plugin replaces the small snippet that looks for `print-pdf`
in the query string. It reacts to the trigger and adds the print stylesheet.

It has a second trigger that materializes the fragments. This mode
clones the slide for each fragment. The first slide will contains the first
fragment, the second the first and the second and so on. The goal is to
create a pdf that can be used to present.

## Options

```JavaScript
{
  trigger: {
    print: 'print-pdf',
    expand: 'print-pdf-expand'
  },
  printCSS: 'path/to/print/style.css'
}
```

All options are optional. 

### trigger.print

String expected in the query string to trigger print output.

### trigger.expand

String expected in the query string to trigger fragment slide expansion. This
will trigger print output as well.

### printCSS 

The plugin will compile the path to the stand reveal.js print stylesheet automatically.
If here is a problem with that, the url can be provided here.
