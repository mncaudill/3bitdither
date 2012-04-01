
3 Bit Dither
==============
Implemented by Nolan Caudill

This particular dither uses the <a href="http://en.wikipedia.org/wiki/Floyd%E2%80%93Steinberg_dithering">Floyd-Steinberg algorithm</a> 
that goes pixel by pixel, rounds the individual R, G, and B channels to either 0x00 or 0xff, and then distributes those differences (which the algorithm calls the "quantization error") in differing amounts to pixels further down the line. This algorithm squeezes your palette down to just 8 colors, while still giving a decent approximation of the original image.

This runs completely client-side, using the FileReader and canvas APIs. If you have a somewhat modern browser, this should work. Also, you can right-click and save the result of the dithering.

