# The QMepa890 database
QM calculated proton affinities (Epa) of 890 molecules from the QM7 database.

## What is in the database:

A bunch of molecules at two different protonation state. Nearly all molecules are amines. Both protonation states are optimized structures, and molecules that undergo rearrangements are removed from the dataset. This includes, but is not limited to: rotation of groups, bond formation, and basically anything I found weird.

### Level of theory:
All structures are optimized at the PBE0/def2-TZVP level of theory in ORCA.
All energies are calculated at the PBE0/def2-TZVP level as well. No RI etc approximations were used.
PM6 heats-of-formation are calculated in MOPAC using the COSMO implicit solvent model with a dielectric constant of `EPS=78.4`.

### Nomenclature of XYZ files:

The database is constructed from a subset of the QM7 database (www.quantum-machine.org), and the File ID corresponds to the same ID in the QM7 database. E.g. the file `0009.xyz` will be identical to molecule 0009 in the QM7 database, and `0009_+.xyz` will be the corresponding protonated state of the same molecule.

### The CSV file:
The CSV file contains the following information

1. File ID (e.g. 0415 means the information pertains to the files `0415.xyz` and `0415_+.xyz`)
2. Index of the proton (in the `XXXX_+.xyz` file listed in the same row)
3. Gas-phase energy of neutral molecule plus thermal corrections from vibrational analysis
4. Gas-phase energy of protonated molecule plus thermal corrections from vibrational analysis
5. Gas-phase energy of neutral molecule
6. Gas-phase energy of protonated molecule
7. Energy of neutral molecule using SMD implicit solvent model
8. Energy of protonated molecule using SMD implicit solvent model
9. PM6 heat-of-formation of neutral molecule using COSMO implicit solvent model
10. PM6 heat-of-formation of protonated molecule using COSMO implicit solvent model

### Units:
Energies are given in units of **kcal/mol**! The XYZ files contain structures contain the coordinates in units of in Ångstrøm.


## Citation:
Please cite this repository. Or don't.

## License:
Licensed under the terms of the CC0 1.0 license.
