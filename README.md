## Image Color Reduction by KMeans

This notebook reduces the number of colors using [scikit learn](http://scikit-learn.org/stable/) [KMeans](http://scikit-learn.org/stable/modules/clustering.html#k-means) algo.
+ Each RGB color is a 3-dimension vector where each dimension can have 256 values (from 0 to 255 included).
+ The KMeans clustering algorithm is used on 10% of randomly selected pixels.
+ Each original pixel is then mapped to the closest cluster center.
+ The resulting image has a (much) smaller number of colors.
+ The number of colors necessary for the human eye to be insensitive to any additional color granularity is what we want to discover here.
+ Because integers are coded as bits, the interesting number of colors are the powers of two: 2, 4, 8, 16, 32, 64, 128, 256, etc.
+ But it is not immediate to go from color reduction to smaller file size as we can see from the file sizes. 

The new [IPywidgets](https://ipywidgets.readthedocs.io/en/latest/) are used to see the result. Very convenient.

