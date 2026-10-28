# Molecular Docking Protocol

## 1. Docking Software

Molecular docking was performed using AutoDock Vina to predict the binding poses of quercetin within the selected binding pocket of DNA gyrase B from *Escherichia coli*.

## 2. Input Files

The following prepared files were used for docking:

| File              | Description                |
| ----------------- | -------------------------- |
| `4kfg.pdbqt`      | Prepared protein receptor  |
| `quercetin.pdbqt` | Prepared quercetin ligand  |
| `config.txt`      | Docking configuration file |

## 3. Grid Box Configuration

A grid box was defined around the selected protein-binding pocket. The centre coordinates (`14.298`, `18.715`, and `-13.137`) and box dimensions (`60`, `60`, and `60`) were specified in the AutoDock Vina configuration file.

The exhaustiveness parameter was set to 8 to control the search effort during docking.

**Note:** The grid centre and dimensions must correspond to the actual binding pocket. Vina box dimensions are specified in ångströms.

## 4. Docking Execution

AutoDock Vina was run using the following command:

`vina --config config2.txt --log log.txt --out output.pdbqt`

The command specifies the receptor, ligand, configuration file, output poses, and docking log.

## 5. Output Files

| Output file    | Description                                       |
| -------------- | ------------------------------------------------- |
| `output.pdbqt` | Predicted ligand-binding poses                    |
| `log.txt`      | Predicted binding-affinity scores and RMSD values |

## 6. Docking Score Analysis

The docking log was examined to compare the predicted binding-affinity scores of the generated poses. The pose with the most negative score was selected as the initial candidate for further structural and interaction analysis.

Docking scores were interpreted as computational predictions and not as experimentally measured binding free energies.
