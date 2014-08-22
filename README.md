[Seeing 3D chairs](http://www.di.ens.fr/willow/research/seeing3Dchairs) source code
===========

Here you will find a Matlab implementation of the algorithm described
in the following paper:

   Mathieu Aubry, Daniel Maturana, Alexei A. Efros, Bryan C. Russell, and Josef Sivic.
   Seeing 3D chairs: exemplar part-based 2D-3D alignment using a large dataset of CAD models.
   CVPR, 2014.
   [PDF](XXX) | [BibTeX](XXX) | [Project page](http://www.di.ens.fr/willow/research/seeing3Dchairs)

Note that this implementation has minor differences with the one used to generate the results shown in the paper.

For any questions or feedback regarding the source code please contact [Mathieu Aubry](mailto:mathieu.aubry@polytechnique.org). 


### DOWNLOADING THE CODE:

You can download a [zip file of the source code](https://github.com/mathieuaubry/seeing3Dchairs/archive/master.zip) directly.  

Alternatively, you can clone it from GitHub as follows:

``` sh
$ git clone https://github.com/mathieuaubry/seeing3Dchairs.git
```


### RUNNING THE CODE:

1. Start by compiling the code.  At the Matlab command prompt run:

   ``` sh
   >> compile;
   ```

2. demoGetAllDEs.m is a script that compute the discriminative elements from a set of rendered views. It must be run before doing detection.

3. demoDetection.m is a script that uses the discriminative elements to detect chairs in a test image. It generates an HTML file visualizing the results after non-maximum suppression.

Both scripts can be used directly for a small number of 3D models, but
should be parallelized to use the full set in reasonable time. The
three functions to parallelize are indicated in the comments of the scripts.

You will need to download the [rendered views of the chair CAD
models](http://www.di.ens.fr/willow/research/seeing3Dchairs/data/rendered_chairs.tar), [HOG whitening parameters](http://www.di.ens.fr/willow/research/seeing3Dchairs/data/whitening_params.mat), and [negative training
examples](http://www.di.ens.fr/willow/research/seeing3Dchairs/data/negative_hogs.mat).

### ACKNOWLEDGMENTS:

The functions features.cc and bboverlap.m  are derived from Ross Girshick and Pedro Felzenswalb implementation available on https://github.com/rbgirshick/voc-dpm 
