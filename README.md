# HPDBSCAN

Highly parallel DBSCAN (HPDBSCAN) is a shared- and distributed-memory parallel implementation of the Density-Based Spatial Clustering for Applications with Noise (DBSCAN) algorithm. It is written in C++ and has been implemented with Ompss-2 tasks.  

## Dependencies

HPDBSCAN requires the following dependencies. Please make sure, that these are installed, before attempting to compile the code.

* C++11 compliant compiler (e.g. g++ 4.8+)
* Ompss-2
* Mercurium compiler (You can find the build requirements, the configuration flags and the instructions to build Mercurium in the following link: https://github.com/bsc-pm/mcxx/blob/master/README.md)

## Usage

The typical basic usage of HPDBSCAN is shown below. It assumes that the application is used in a typical high-performance computing setup with multiple distributed nodes and processing cores per node. The data is passed to the application in form of an HDF5 file with 'Data' being the input dataset and results stored in 'out.csv'. 

``` 
Highly parallel DBSCAN clustering algorithm
Usage:
  ./dbscan [OPTION...]

  -m, --minPoints arg       density threshold (default: 2)
  -e, --epsilon arg         spatial search radius (default: 0.1)

```


## Reference

```
Götz, M., Bodenstein, C., Riedel M.,
HPDBSCAN: highly parallel DBSCAN,
Proceedings of the Workshop onf Machine Learning in High-Performance Computing Environments, ACM, 2015.
https://bitbucket.org/markus.goetz/hpdbscan/src/default/
```

