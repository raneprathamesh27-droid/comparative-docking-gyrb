# Ligand Preparation Protocol

## 1. Ligand Retrieval

The three-dimensional structure of quercetin was retrieved from the PubChem database. The compound was searched by name, and its 3D conformer was downloaded in SDF format.

**Compound:** Quercetin
**PubChem CID:** 5280343
**Source:** [PubChem](https://pubchem.ncbi.nlm.nih.gov/compound/5280343)

## 2. Ligand Format Conversion

The downloaded SDF file was opened in PyMOL. The ligand structure was then exported in PDB format for further preparation using AutoDockTools (MGL Tools).

## 3. Ligand Preparation Using AutoDockTools

The ligand PDB file was loaded into AutoDockTools. The ligand preparation procedure was performed to generate a structure suitable for molecular docking. The prepared ligand was saved in PDBQT format as `quercetin.pdbqt`.

## 4. Output File

| Parameter                | Details                   |
| ------------------------ | ------------------------- |
| Ligand                   | Quercetin                 |
| PubChem CID              | 5280343                   |
| Initial file format      | SDF                       |
| Intermediate file format | PDB                       |
| Final file format        | PDBQT                     |
| Visualization software   | PyMOL                     |
| Preparation software     | AutoDockTools (MGL Tools) |
| Prepared ligand file     | `quercetin.pdbqt`         |

## 5. Methodological Note

The prepared ligand file was used as the ligand input for AutoDock Vina during molecular docking with DNA gyrase B from *Escherichia coli*.
