<img src="https://github.com/mastodon-sc/mastodon-documentation/blob/1bb4e313a01a310bd29478842df1405d220fad2b/docs/imgs/Mastodon-logo_jy-01.png" width="250" align="center">

# About Mastodon.

> :warning: This organization refers to Mastodon: the open-source scientific software for tracking cells and line aging in large microscopy generated in Life-Sciences. It does not refer to Mastodon: the decentralized social network. For the latter, please refer to [https://github.com/mastodon](https://github.com/mastodon)


Mastodon is a large-scale tracking and track-editing framework for large, multi-view images, such as the ones that are typically generated in the domain Development Biology or Stem-Cell Biology or Cell Biology.

Why using Mastodon?

Modern microscopy technologies such as light sheet microscopy allows live sample *in toto* 3D imaging with high spatial and temporal resolution. 
Such images will be 3D over time, possibly multi-channels and multi-view. 
Computational analysis of these images promises new insights in cellular, developmental and stem cells biology. 
However, a single image can amount to several terabytes, and in turn, the automated or semi-automated analysis of these large images can generate a vast amount of annotations. 
The challenges of big data are then met twice: first by dealing with a very large image, and second with generating large annotations from this image. 
They will make interacting and analyzing the data especially difficult.

**Mastodon** is our effort to provide a tool that can harness these challenges. 
You can find the user and developer documentation [here](https://mastodon.readthedocs.io/).

This page describes the repositories of this organization and list maintainers and responsibilities.

### Repositories and responsibilities. 

Mastodon tries to offer at the same time 
- A Java library for manipulating collections and mathematical graphs containing a very large number of objects.
- A scientific application ('Mastodon') that uses this library to offer Researchers of Life-Sciences a user-friendly tool to perform cell tracking and lineaging in large movies.
- Several optional modules and contributions that extend the features of the Mastodon application.

This results in having about 10 repositories in this organization, that we list and describe briefly in the  below.

| Repository                                                                                | Description                                                                                                                                                                                                             | Maintainer          | Distribution                                              |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | --------------------------------------------------------- | --- |
| [`mastodon-collection`](https://github.com/mastodon-sc/mastodon-collection)               | Core Mastodon repository containing the library to manipulate collections containing a large number of objects efficiently. Offers data locality and garbage-collection free programming. Based on the `Trove` library. | TP, JYT, MA         | In the Fiji update site "Mastodon"                        |
| [`mastodon-graph`](https://github.com/mastodon-sc/mastodon-graph)                         | A Java library to create and manipulate (mathematical) graphs containing a large number of vertices and edges. Based on Mastodon-collection                                                                             | TP, JYT, MA         | In the Fiji update site "Mastodon"                        |
| [`mastodon`](https://github.com/mastodon-sc/mastodon)                                     | The main repository for the Mastodon application. Based on Mastodon-collection and Mastodon-graph.                                                                                                                      | TP, JYT, MA, VU, KS | In the Fiji update site "Mastodon"                        |
| [`mastodon-tracking`](https://github.com/mastodon-sc/mastodon-tracking)                   | Automated tracking algorithms for Mastodon                                                                                                                                                                              | TP, JYT             | In the Fiji update site "Mastodon"                        |
| [`mastodon-selection-creator`](https://github.com/mastodon-sc/mastodon-selection-creator) | Mastodon plugin to create selections from mathematical expressions.                                                                                                                                                     | JYT                 | In the Fiji update site "Mastodon"                        |
| [`mastodon-ellipsoid-fitting`](https://github.com/mastodon-sc/mastodon-ellipsoid-fitting) | Mastodon plugin that can robustly fit a 3D ellipsoid on noisy data of _e.g._ nuclei images.                                                                                                                             | TP, JYT             | In the Fiji update site "Mastodon"                        |
| [`mastodon-pasteur`](https://github.com/mastodon-sc/mastodon-pasteur)                     | Small collection of plugins developed for the research led in the Institut Pasteur, Paris, but of general utility.                                                                                                      | JYT                 | In the Fiji update site "Mastodon"                        |
| [`mastodon-tomancak`](https://github.com/mastodon-sc/mastodon-tomancak)                   | Small collection of plugins developed for the research led of Pavel Tomancak, MPI-CBG, Dresden, but of general utility.                                                                                                 | TP, VU              | In the Fiji update site "Mastodon"                        |
| [`mastodon-app`](https://github.com/mastodon-sc/mastodon-app)                             | Scripting interface for Mastodon in the script editor of Fiji. Depends on all the repos above.                                                                                                                          | JYT                 | In the Fiji update site "Mastodon"                        |     |
| [`mastodon-documentation`](https://github.com/mastodon-sc/mastodon-documentation)         | Source files for the online documentation.                                                                                                                                                                              | JYT                 | On ReadTheDocs, [here](https://mastodon.readthedocs.io/). |     |
| [`mastodon-collaborative`](https://github.com/mastodon-sc/mastodon-collaborative)         |                                                                                                                                                                                                                         | VU                  |                                                           |     |
| [`mastodon-ctc`](https://github.com/mastodon-sc/mastodon-ctc)                             |                                                                                                                                                                                                                         | VU                  |                                                           |     |
| [`mastodon-ext-viewers`](https://github.com/mastodon-sc/mastodon-ext-viewers)             |                                                                                                                                                                                                                         | VU                  |                                                           |     |
| [`mastodon-sciview`](https://github.com/mastodon-sc/mastodon-sciview)                     |                                                                                                                                                                                                                         | VU                  |                                                           |     |
| [`matlab-mastodon-importer`](https://github.com/mastodon-sc/matlab-mastodon-importer)     | Several MATLAB functions to import Mastodon files into MATLAB.                                                                                                                                                          | JYT                 | Download from repo.                                       |     |
| [`matlab-example-data`](https://github.com/mastodon-sc/matlab-example-data)               | An example Mastodon dataset imported from the [TGMM framework](https://bitbucket.org/fernandoamat/tgmm-paper/src/master/).                                                                                              | TP                  |                                                           |     |

Maintainers:

- TP: Tobias Pietzsch
- JYT: Jean-Yves Tinevez
- MA: Matthias Arzt 
- VU: Vladimír Ulman
- KS: Ko Sugawara
