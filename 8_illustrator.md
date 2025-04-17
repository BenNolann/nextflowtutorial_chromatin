---
layout: default
title: Illustrator
---


You've run a nextflow pipeline, perform some data analysis and now you've got a bunch of figures. Your next step is to put them together in a figure panel to tell a story for a paper or presentation.

## Image types

### Raster versus Vectorized images

[From Adobe themselves:](https://www.adobe.com/creativecloud/file-types/image/comparison/raster-vs-vector.html)

**Raster**: Raster files are images built from pixels — tiny color squares that, in great quantity, can form highly detailed images such as photographs. The more pixels an image has, the higher quality it will be, and vice versa. The number of pixels in an image depends on the file type (for example, JPEG, GIF, or PNG).

**Vector**: Vector files use mathematical equations, lines, and curves with fixed points on a grid to produce an image. There are no pixels in a vector file. A vector file’s mathematical formulas capture shape, border, and fill color to build an image. Because the mathematical formula recalibrates to any size, you can scale a vector image up or down without impacting its quality.
(for example, SVG, PDF).

### Difference

1. *Resolution:* If you zoom in on a raster file, you will start to see the pixels that it is made up of. It becomes 'blurry'. Raster files have greater color range and allow better color editing. Vector images do not have a resolution images, you can zoom in indefinitely without losing quality. 

NOTE: This is the key difference between Photoshop and Illustrator. The former is designed for working with Raster images whilst the latter is for vector images. Although you can still import raster images (png/jpg) into illustrator, with the caveat of resolution.

2. *Uses:* Digital photographs are usually raster files. Many digital cameras automatically shoot and save photos as raster files — and the images you see online are often rasters, too. Raster files are also commonly used for editing images, photos, and graphics. Vector files work better for digital illustrations, complex graphics, and logos. That’s because the resolution of vectors remains the same when resized, making them suitable for a wide variety of printed formats. Some projects combine both raster and vector images. For example, a brochure may use vector graphics for the company logo but raster files for photography.

All this to say, you will likely be working with both raster and vector images in your time. But when generating images from R or Python or whatever tool you're using, think about how you're going to work with that image. 

Can this tool export an image as an 'svg'? If so, it makes working with it in Illustrator a lot easier. 

## Combine the below images into a figure panel. 

* 

Open up Illustrator, create a new file and import these images in.

In your figure panel, complete the following tasks:

1. Arrange the images in a way that tells a story.
2. Create a diagram for the experimental design (Doesn't have to be real)
3. Create a final model describing the biological process (Also doesn't have to be real).
4. Export the image as a png.