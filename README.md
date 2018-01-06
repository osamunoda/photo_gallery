# photo_gallery

In FileMaker16(Mac) accsessing local files from webviewer is limited. But FileMaker itself can still access local files.
This means that webviewer can access local files via FileMaker.

(HowTo)
First, make a calculation field: unstored, (definition) $$src
Second, In the webviewer definition set the image path to $$src like below
  ex: absolute path    image:/Macintosh HD/Users/userName/pictures/sample.jpg
      relative path    image:../pictures/sample.jpg
Third: Get the base64 of the taget image from the calculation field(First step) using Base64EncodeRFC function, and embed it in the html/javascript code!

See the sample file( alternative_img_not_shown.fmp12)

================================================

This file, photo_gallery.fmp12 is made using this technique.
Specify the image folder by dialog, then images(jpg/png) in that directory are listed horizontally.
