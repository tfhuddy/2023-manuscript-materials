# 2023-manuscript-materials
One item here is a dummy pdb, which is an example of a straight alpha helix structure. 

This is used as a dummy input (it will be replaced by helical backbones freshly generated from Crick parameters) to Rosetta (tested with Rosetta 3.13 (https://rosettacommons.org/) on Ubuntu 22.04), and is processed using the example script provided.

Test case usage:

(1) Have 6 GB of cpu memory available and the Rosetta command-line-interface executable installed, and the loop fragment database downloaded (files.ipd.uw.edu/pub/modular_repeat_protein_2020/ss_grouped_vall_all.h5)

(2) Run example script to produce a linear THR backbone example:

/path/to/your/rosetta/install/main/source/bin/rosetta_scripts.hdf5.linuxgccrelease -indexed_structure_store:fragment_store=/path/to/your/downloaded/loop/fragment/database.h5 -parser:protocol example.xml -s dummy.pdb -corrections::beta_nov16 true

(3) Edit annotated parameters in the example.xml to vary the geometry of the THR that is produced
