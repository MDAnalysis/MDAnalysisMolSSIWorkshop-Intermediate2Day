# Project Ideas for MDAKits Hackathon

While at the hackathon you can work on anything you want --- all the
developers are here to support you to build something amazing. If you
want some inspiration, here are some ideas that the wider MDAnalysis
community would really want to see. These ideas are in _random order_.


## Trajectory clustering ##

It is common to use unsupervised learning algorithms to cluster a
trajectory by similarity to discover different states.

A typical approach is to first calculate the RMSD of a structure with
itself across all trajectory frames, forming a $T \times T$ symmetric
RMSD matrix where $T$ is the number of frames in the
trajectory. However, any other [metric][] (or distance) instead of
RMSD will also work if you can produce a suitable _similarity matrix_.

One can then use any number of [clustering][] algorithms to partition
the similarity matrix and thus assign different cluster numbers to the
different frames of the trajectory. 

The [mdaencore](https://www.mdanalysis.org/mdaencore/) MDAKit for Ensemble Similarity Calculations 
also implements some clustering methods (namely, Affinity Propogation and 
DBSCAN/KMeans, via scikit-learn; as described 
[in the docs here](https://www.mdanalysis.org/mdaencore/autosummary/mdaencore.clustering.ClusteringMethod.html#module-mdaencore.clustering.ClusteringMethod)).
However, a general-use cluster analysis tool, featuring a larger 
selection of clustering algorithms would likely be useful to many users.

Clustering methods could include -

* [scikit-learn clustering][] contains _many_ clustering algorithms
  that can be either used with a similarity matrix or directly with
  trajectory data like coordinates.
  
* The GROMOS clustering algorithm is widely used in biomolecular
  simulations [[Daura 1999]](#Daura1999). (See Issue
  [#2876](https://github.com/MDAnalysis/mdanalysis/issues/2876).)
  
  The following excerpt from Daura et al. describes the algorithm:
  
    "To find clusters of structures in a trajectory the RMSD of atom
    positions between all pairs of structures was determined. For each
    structure the number of other structures for which the RMSD was
    0.1 nm or less (backbone, residues 2 ± 6) for structure 1 or 0.08
    nm or less (backbone, residues 2 ± 5) for structure 2 (neighbor
    conformations) was calculated. The structure with the highest
    number of neighbors was taken as the center of a cluster, and
    formed together with all its neighbors a (first) cluster. The
    structures of this cluster were thereafter eliminated from the
    pool of structures. The process was repeated until the pool of
    structures was empty. In this way, a series of nonoverlapping
    clusters of structures was obtained."

### Objectives ###

- Create a `ClusterAnalysis` class that allows the user to run any of
  the [scikit-learn clustering][] algorithms that can work on raw
  data (such as K-means). Use the `AnalysisBase` framework to write
  the analysis class (see the [tutorial on writing your own
  trajectory analysis][UserGuide AnalysisBase].
- Create an MDAKit that makes `ClusterAnalysis` available.
- Implement additional clustering methods such as GROMOS clustering
  [[Daura 1999]](#Daura1999) (described above in more detail).


### References ###

1. <a id="Daura1999"/>X Daura, K Gademann, B Jaun, D Seebach, WF van Gunsteren, and AE Mark. Peptide folding: When simulation meets experiment. Angew. Chem. Int. Ed., 38(1-2):236–240, 1999. doi: [10.1002/(SICI)1521-3773(19990115)38:1/2<236::AID-ANIE236>3.0.CO;2-M](https://doi.org/10.1002%2F%28SICI%291521-3773%2819990115%2938%3A1%2F2%3C236%3A%3AAID-ANIE236%3E3.0.CO%3B2-M).

[metric]: https://en.wikipedia.org/wiki/Metric_space#Definition
[clustering]: https://en.wikipedia.org/wiki/Cluster_analysis
[scikit-learn clustering]: https://scikit-learn.org/stable/modules/clustering.html
[UserGuide AnalysisBase]: https://userguide.mdanalysis.org/stable/examples/analysis/custom_trajectory_analysis.html


## State-based density analysis ##

Calculations of densities of solvent or ligands with the 
[MDAnalysis.analysis.density][] code can be a powerful way to
obtain a global picture of solvent/ligand behavior in relationship
to, e.g., a protein. Sometimes there are changes in the protein
that lead to a different density but when averaged over the whole
trajectory, the changes in the density are averaged out and are
less clear. It is therefore useful to generate densities only
for parts of the trajectory that correspond to a specific
**state** of the system.

For our purpose here, a **state is a collection of trajectory frames**.
Each frame only belongs to a single state.

States can be identified in many difference ways. 
* For example, we can look at the conformation of the protein itself
  and use clustering by protein RMSD (see Project above). But we 
  can also cluster by ligands or specific sidechains: select
  small molecule/ion binding sites or sidechain configurations by a
  ligning to a ‘fixed’ reference (e.g. protein) and perform 
  clustering using the coordinates of the group of interest.
* Compute some form of _order parameter_ and assign different states
  based on the order parameter (e.g., a distance that describes when
  a protein is in an "open" conformation (distance greater than a
  cutoff) and a "closed" conformation (distance smaller than a cutoff)),
  or a distance that indicates when a small molecule is bound/not bound.

### Objectives ###
1. Create an analysis class that takes as input a list of states
   (e.g., a dict stateID -> list of trajectory frames, or a a list of lists
   where state 0 corresponds to list 0, state 1 to list 1, etc...)
   and then creates a density for each state (making use of the existing
   [MDAnalysis.analysis.density.DensityAnalysis][]; note the `frames` keyword
   of the [`run()`][MDAnalysis.analysis.density.DensityAnalysis.run()] method,
   which takes a list of trajectory *frames*).
3. Optimize the approach so that you don't have to run `DensityAnalysis`
   separately for each state.


[MDAnalysis.analysis.density]: https://docs.mdanalysis.org/stable/documentation_pages/analysis/density.html
[MDAnalysis.analysis.density.DensityAnalysis]: https://docs.mdanalysis.org/stable/documentation_pages/analysis/density.html#MDAnalysis.analysis.density.DensityAnalysis
[MDAnalysis.analysis.density.DensityAnalysis.run()]: https://docs.mdanalysis.org/stable/documentation_pages/analysis/density.html#MDAnalysis.analysis.density.DensityAnalysis.run


## New file formats ##

MDAnalysis supports a wide range of file formats for reading/writing 
coordinates and topologies 
(https://userguide.mdanalysis.org/stable/formats/index.html). 
However, there are still some file formats that are missing - e.g.
[PDBx/mmCIF][], which has replaced the PDB format as the default 
format for the Protein Data Bank (see Issue
[#2367](https://github.com/MDAnalysis/mdanalysis/issues/2367)).
We also welcome the addition of support for any other file formats 
we are currently missing.

Note that MDAnalysis can support new formats _without adding code to
the main package_. You can put the code ("reader" and "writer" 
classes for trajectories, "parser" classes for topologies) into a MDAKit and 
if you use the appropriate base classes, MDAnalysis will automagically
know how to work with the newly supported file format!

### Where to start

- Identify a file format currently not supported by MDAnaylsis --- if you
  don't have a particular format in mind, support for PDBx/mmCIF is a
  frequent request.

  (See the [PDBx/mmCIF software resources][], for example,
  [py-mmcif][] and [biopython][] could also be used, and there exists a Python-only
  implementation in [mmcif_pdbx][].)
- Become familiar with our reader/writer API - for
  [trajectory files (coordinate data)](https://docs.mdanalysis.org/stable/documentation_pages/coordinates/init.html)
  and [topology files (atom information)](https://docs.mdanalysis.org/stable/documentation_pages/topology_modules.html)
  as appropriate; and look at how existing supported file formats
  are handled.
- Create a Kit featuring a new reader/writer class, using `ReaderBase`/`WriterBase`,
  for the new file format. If there are existing tools that could
  aid in reading this format, your Kit could use these as dependencies.


[PDBx/mmCIF]: https://pdb101.rcsb.org/learn/guide-to-understanding-pdb-data/beginner%E2%80%99s-guide-to-pdb-structures-and-the-pdbx-mmcif-format

[PDBx/mmCIF software resources]: https://mmcif.wwpdb.org/docs/software-resources.html

[py-mmcif]: https://github.com/rcsb/py-mmcif

[biopython]: https://biopython.org/

[mmcif_pdbx]: https://github.com/Electrostatics/mmcif_pdbx



## Contact analysis ##

Identifying inter- and intra-molecular contacts is the basis of many 
simulation analyses. A pair of atoms is often defined as “in contact” 
when they fall within a specified cut-off distance of each other. 

*Native contact analysis* identifies the contacts present in a reference
structure, and then tracks the existence of these contacts across a 
trajectory; evolution of the fraction of native contacts can be used to 
analyse protein folding, binding or other conformational changes. 
MDAnalysis features a [Native contacts analysis module]() that allows 
this fraction of native contacts to be calculated over a trajectory. 
However, the native contact approach is limited - a reference structure 
must be defined, only contacts present in the reference structure are 
considered, and only the total fraction of contacts is tracked, 
not individual pairs.

MDAnalysis also features a [hydrogen bond analysis module]() which does
allow the identification of all contacts across all frames, without
the need for a reference structure, but is geared towards the 
the identification of hydrogen bonds. A more generalised analysis 
could be useful to many MDAnalysis users. 

### Where to start
- Look at the existing Native Contact and Hydrogen bond analysis modules
  to see how existing contact analysis is performed
- Create a class using `AnalysisBase` (see the guide on User Guide on
  [custom trajectory analysis]() that identifies all contacts in each frame,
  e.g. generalising the approach used by `hbond_analysis`. 
- Additional features could include e.g. tools to allow extraction of
  timeseries data for a specified contact pair from the full contact/frame
  array.

[Native contacts analysis module]: https://docs.mdanalysis.org/stable/documentation_pages/analysis/contacts.html
[hydrogen bond analysis module]: https://docs.mdanalysis.org/stable/documentation_pages/analysis/hydrogenbonds.html#MDAnalysis.analysis.hydrogenbonds.hbond_analysis.HydrogenBondAnalysis.hbonds
[custom trajectory analysis]: https://userguide.mdanalysis.org/stable/examples/analysis/custom_trajectory_analysis.html



## Voronoi tessellation ##

A [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram) is 
the division of a space into regions around a set of seed points such 
that each point in a given region is closer to that seed point than 
any other. Voronoi tessellations can be used in various density and 
spatial analysis, e.g. for characterizing membranes or interaction 
surfaces/binding sites. 

Voronoi tessellation and related algorithms (e.g. Delaunay triangulation) 
have been implemented in scipy (https://docs.scipy.org/doc/scipy/reference/spatial.html#delaunay-triangulation-convex-hulls-and-voronoi-diagrams).


## Ring puckering ##

Ring groups can adopt a variety of “puckered” geometries that influence 
their physical and chemical properties. Several formulations exist for 
quantifying this puckering, e.g. Pickett angles [[Strauss 1970]](#Strauss1970), 
Cremer-Pople [[Cremer 1975]](#Cremer1975), and Hill-Reilly [[Hill 2007]](#Hill2007).

MDAnalysis currently features tools for assessing puckering in 5-membered 
rings in our [nucleic acid analysis module](https://docs.mdanalysis.org/stable/documentation_pages/analysis/nuclinfo.html); 
however, such capabilities are lacking for 6 (or higher) membered rings.


### References
1. <a id="Strauss1970"/>Strauss, H.L.; Pickett, H.M; Conformational structure, energy and inversion rates of cyclohexane and some related oxanes. J. Am. Chem. Soc. 1970, 92: 7281-7290 https://doi.org/10.1021/ja00728a009
2. <a id="Cremer1975"/>Cremer D., Pople, J.A.; General definition of ring puckering coordinates. J. Am. Chem. Soc 1975, 97: 1354-1358 https://doi.org/10.1021/ja00839a011
3. <a id="Hill2007"/>Hill, A. D.; Reilly, P. J. Puckering Coordinates of Monocyclic Rings by Triangular Decomposition. J. Chem. Inf. Model. 2007, 47: 1031– 1035 https://doi.org/10.1021/ci600492e
