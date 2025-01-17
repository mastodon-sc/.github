<img src="https://github.com/mastodon-sc/mastodon-documentation/blob/1bb4e313a01a310bd29478842df1405d220fad2b/docs/imgs/Mastodon-logo_jy-01.png" width="250" align="center">

# About Mastodon.

> :warning: This organization refers to Mastodon: the open-source scientific software for tracking cells and lineaging in large microscopy images generated in Life-Sciences. It does not refer to Mastodon: the decentralized social network. For the latter, please refer to [https://github.com/mastodon](https://github.com/mastodon)


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

This results in having more than 10 repositories in this organization, that we list and describe briefly in the below.

#### Core artifacts and repositories.

These repos correspond to the core Mastodon app, that you will get in Fiji with the "Mastodon" update site. It ships the full core functionalities need to visualize, edit, track and linages large images. 

| Repository                                                   | Description                                                  | Maintainer          | Distribution                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------------------------------------------------------------ |
| [`mastodon-collection`](https://github.com/mastodon-sc/mastodon-collection) | Core Mastodon repository containing the library to manipulate collections containing a large number of objects efficiently. Offers data locality and garbage-collection free programming. Based on the `Trove` library. | TP, JYT, MA         | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-graph`](https://github.com/mastodon-sc/mastodon-graph) | A Java library to create and manipulate (mathematical) graphs containing a large number of vertices and edges. Based on `mastodon-collection`. | TP, JYT, MA         | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon`](https://github.com/mastodon-sc/mastodon)        | The main repository for the Mastodon application. Based on `mastodon-collection` and `mastodon-graph`. | TP, JYT, MA, VU, KS | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-tracking`](https://github.com/mastodon-sc/mastodon-tracking) | Automated tracking algorithms for Mastodon.                  | TP, JYT             | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-selection-creator`](https://github.com/mastodon-sc/mastodon-selection-creator) | Mastodon plugin to create selections from mathematical expressions. | JYT                 | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-ellipsoid-fitting`](https://github.com/mastodon-sc/mastodon-ellipsoid-fitting) | Mastodon plugin that can robustly fit a 3D ellipsoid on noisy data of _e.g._ nuclei images. | TP, JYT             | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-pasteur`](https://github.com/mastodon-sc/mastodon-pasteur) | Small collection of specific plugins of general use, such as nearest-neighbors statistics and CSV importer. | JYT                 | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |
| [`mastodon-app`](https://github.com/mastodon-sc/mastodon-app) | Scripting interface for Mastodon in the script editor of Fiji. Depends on all the repos above. | JYT                 | In the [Fiji update site](https://imagej.net/update-sites/) "Mastodon" |

#### Documentation.

Repositories related to documenting Mastodon, tutorials and code examples. 

| Repository                                                   | Description                                                  | Maintainer          | Distribution                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------------------------------------------------------------ |
| [`mastodon-documentation`](https://github.com/mastodon-sc/mastodon-documentation) | Source files for the online documentation.                   | JYT                 | On ReadTheDocs, [here](https://mastodon.readthedocs.io/).    |
| [`mastodon-plugin-example`](https://github.com/mastodon-sc/mastodon-plugin-example) | Example code used to document how to extend Mastodon with custom plugins, features and detectors. | JYT                 | On a specific ReadTheDocs section, [here](https://mastodon.readthedocs.io/en/latest/docs/partD/mastodon_data_structures.html) |
| [`mastodon-example-data`](https://github.com/mastodon-sc/mastodon-example-data) | Example data set to demonstrate the Mastodon functionality.  | TP                  | Download from repo.                                         |

#### Interoperability.

Repositories related to exchanging Mastodon data with other software, languages, etc.

| Repository                                                   | Description                                                  | Maintainer          | Distribution                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------------------------------------------------------------ |
| [`matlab-mastodon-importer`](https://github.com/mastodon-sc/matlab-mastodon-importer) | Several MATLAB functions to import Mastodon files into MATLAB. | JYT                 | Download from repo.                                          |
| [`python-mastodon-importer`](https://github.com/mastodon-sc/python-mastodon-importer) | Mastodon Reader for Python. Import the spots and links tables, features, tags and meta data from a Mastodon project file. | CS                  | Pip.                                                         |

#### Extra functionalities.

Optional repositories that bring additional and specific functionalities to Mastodon. Some of them are experimental. 

| Repository                                                   | Description                                                  | Maintainer          | Distribution                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------------------------------------------------------------ |
| [`mastodon-tomancak`](https://github.com/mastodon-sc/mastodon-tomancak) | Collection of plugins for editing and analyzing tracking data. Developed for the research in the lab of Pavel Tomancak, MPI-CBG, Dresden, but of general utility. | MA, VU, TP, SH      | In the [Fiji update site](https://imagej.net/update-sites/) ["Mastodon-Tomancak"](https://sites.imagej.net/Mastodon-Tomancak)/ |
| [`mastodon-git`](https://github.com/mastodon-sc/mastodon-git) | Versioning and collaborative editing of a Mastodon projection. (Currently under developement. Uses git for data vesioning and data exchange) | MA                  | In the [Fiji update site](https://imagej.net/update-sites/) ["Maarzt"](https://sites.imagej.net/Maarzt) |
| [`mastodon-blender-view`](https://github.com/mastodon-sc/mastodon-blender-view) | A Mastodon plugin that allows vizualizing cell tracking data interactively in 3D in Blender | MA, SH              | In the [Fiji update site](https://imagej.net/update-sites/) ["Mastodon-Tomancak"](https://sites.imagej.net/Mastodon-Tomancak/) |
| [`mastodon-ctc`](https://github.com/mastodon-sc/mastodon-ctc) | Plugins into Mastodon and Fiji related to the [Cell Tracking Challenge](http://celltrackingchallenge.net/). | VU                  | In the [Fiji update site](https://imagej.net/update-sites/) ["CellTrackingChallenge"](https://sites.imagej.net/Ulman/) |
| [`mastodon-ext-viewers`](https://github.com/mastodon-sc/mastodon-ext-viewers) | Collection of Mastodon plugins that are enabling online transfers of the tracking data (mostly lineage trees) outside Mastodon (usually into sciview or Blender). | VU                  | In the [Fiji update site](https://imagej.net/update-sites/) ["xulman"](https://sites.imagej.net/xulman) |
| [`mastodon-sciview (v2)`](https://github.com/xulman/mastodon-sciview-take2) | Mastodon plugin that starts [sciview](https://github.com/scenerygraphics/sciview) in the same session, and shares and displays image and tracking data directly in it. Allows for editing tracking data from the sciview. | VU, SP              | Download from repo.                                          |
| [`mastodon-deep-lineage`](https://github.com/mastodon-sc/mastodon-deep-lineage) | Collection of plugins to analyse tracking data and some import / export tools. | SH                  | In the [Fiji update site](https://imagej.net/update-sites/) ["Mastodon-DeepLineage"](https://sites.imagej.net/Mastodon-DeepLineage/) |


Maintainers:

- TP: Tobias Pietzsch
- JYT: Jean-Yves Tinevez
- MA: Matthias Arzt 
- VU: Vladimír Ulman
- KS: Ko Sugawara
- SH: Stefan Hahmann
- SP: Samuel Pantze
- CS: Christoph Sommer

# More Documentation

* [Mastodon intro on ImageJ.net](https://imagej.net/plugins/mastodon)
* [Mastodon usage guide on readthedocs](https://mastodon.readthedocs.io/en/latest/index.html)

# Community

* If you have questions regarding usage of Mastodon, we invite you to use the [forum on imagesc](https://forum.image.sc/). You may search for Mastodon related topics using the hashtag `#mastodon` or create a new topic.

# Contribute

## Forum

* For questions related to Mastodon development, please use the [zulip chat](https://imagesc.zulipchat.com/#narrow/stream/327470-Mastodon).

## License Agreement

All contributions like will fall under the "BSD 2-Clause (Simplified) License" as described in the [LICENSE](LICENSE.txt) file.

## Code formatting

We use the Eclipse code formatter. You can find the configuration file [here](https://raw.githubusercontent.com/scijava/scijava-coding-style/1dc9f9467cbdfbde8fb8e40379447baa9abb3f68/src/main/resources/eclipse-formatter-settings/mastodon-coding-style.xml). Please use this formatter for your pull requests.

Users of IntelliJ IDEA can use the [Eclipse Code Formatter Plugin](https://plugins.jetbrains.com/plugin/6546-eclipse-code-formatter) to automatically format your code.

We recommend to use Auto-Format on Save in your IDE, preferably only on changed lines.

