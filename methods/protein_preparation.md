# Protein Preparation Protocol

## 1. Protein Structure Retrieval

The crystal structure of DNA gyrase B from *Escherichia coli* was obtained from the RCSB Protein Data Bank using PDB ID **4KFG**. The downloaded structure was saved in PDB format as `4kfg.pdb`.

**Source:** [RCSB Protein Data Bank](https://www.rcsb.org/structure/4KFG)

## 2. Protein Preparation

The protein structure was opened in AutoDockTools (MGL Tools). Water molecules were removed, and hydrogen atoms were added. Kollman charges were then assigned to prepare the receptor for molecular docking.

## 3. Receptor File Generation

After preparation, the protein was saved in PDBQT format as `4kfg.pdbqt`. This file was used as the receptor input for AutoDock Vina.

## 4. Output File

| Parameter              | Details                   |
| ---------------------- | ------------------------- |
| Target protein         | DNA gyrase B              |
| Organism               | *Escherichia coli*        |
| PDB identifier         | 4KFG                      |
| Original file          | `4kfg.pdb`                |
| Prepared receptor file | `4kfg.pdbqt`              |
| Preparation software   | AutoDockTools (MGL Tools) |

## 5. Methodological Note

Protein preparation was performed to generate a receptor structure suitable for molecular docking. The prepared receptor file was subsequently used in the docking procedure with quercetin.
