
3 Bit Dither
==============
Implemented by Nolan Caudill

            <p>This demo currently uses two different error-diffusion dithering algorithms: <a href="http://verlagmartinkoch.at/software/dither/index.html">Atkinson's</a> and the <a href="http://en.wikipedia.org/wiki/Floyd%E2%80%93Steinberg_dithering">Floyd-Steinberg</a> algorithm.

            <p>Error-diffusion means that the algorithm goes pixel by pixel, rounds the individual R, G, and B channels to either 0x00 or 0xff, and then distributes those differences (which the algorithm calls the "quantization error") in differing amounts to pixels further down the line. It being a 3-bit dithering means that your red, blue, and green channels are represented by a single bit (off or on), giving you a total of 8 colors.</p>

            <p>The demo also does halftone dithering and Bayer dithering (just 2 bit) which don't use error-diffusion, which for these two makes the patterns evident that error-diffusion usually lessens.</p>

<p>This runs completely client-side, using the FileReader and canvas APIs. If you have a somewhat modern browser, this should work. Also, you can right-click and save the result of the dithering.</p>

The demo lives <a href="http://mncaudill.github.com/3bitdither/">here</a>.
