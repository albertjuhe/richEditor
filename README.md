Rich Editor Plugin
==================

This plugin allow you to use Tinymce 4.0 in the annotator editor.

##Installation

To use the tool you need to install the [Annotator plugin](https://github.com/okfn/annotator/) to annotate text. 
Download Tinymce 4.0 and add the PLug-in in the Html file $('body').annotator().annotator('addPlugin', 'RichEditor');

```html
    <script src="../lib/jquery-1.9.1.js"></script>
    <script src="../lib/annotator-full.1.2.9/annotator-full.min.js"></script>
    <!-- For show the annotation creation date -->
    <script src="../lib/jquery.dateFormat.js"></script>
   
    <script src="../lib/tinymce/tinymce.min.js"></script>
    <!-- annotator -->
    <link rel="stylesheet" href="../lib/annotator-full.1.2.9/annotator.min.css">
    <link rel="stylesheet" href="../src/css/style.css">
    <!-- anotator plug in -->
    <script src="../src/richEditor.js"></script>
    <script>
      jQuery(function ($) {
                   var annotator = $('body').annotator().annotator().data('annotator');
                    var propietary = 'demoUser';
                    annotator.addPlugin('Permissions', {
                        user: propietary,
                        permissions: {
                            'read': [propietary],
                            'update': [propietary],
                            'delete': [propietary],
                            'admin': [propietary]
                     },
                     showViewPermissionsCheckbox: true,
                     showEditPermissionsCheckbox: false
                    });
                  $('body').annotator().annotator('addPlugin', 'RichEditor');
                
                  
               });
  </script>
```

##Usage

When you create an annotations a Rich Editor is displayed (TinyMCE).

##Demo
Demo in demo/anotacions.html
