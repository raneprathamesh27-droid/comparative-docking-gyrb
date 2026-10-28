# comparative-docking-gyrb
**Comparative molecular docking and interaction analysis of natural flavonoids against bacterial DNA gyrase B.**
**1. Project Overview**
 
This project investigates the predicted binding of quercetin, a naturally occurring plant flavonoid, to DNA gyrase subunit B (GyrB) of Escherichia coli using molecular docking and protein–ligand interaction analysis.

DNA gyrase is an essential bacterial enzyme involved in regulating DNA topology during replication, transcription, and other DNA-associated processes. Its B subunit contains an ATP-binding domain that contributes to the enzyme's catalytic activity, making this domain a relevant target for computational inhibitor screening.

The study will use an experimentally determined protein structure obtained from the RCSB Protein Data Bank and a three-dimensional quercetin structure retrieved from PubChem. Molecular docking will be performed using AutoDock Vina, followed by analysis of the predicted binding pose and interactions using PyMol.

The project aims to assess the structural possibility of quercetin binding to the selected protein pocket.

**2. Research Question**

Can quercetin be computationally positioned within the ATP-binding region of Escherichia coli DNA gyrase B, and what predicted molecular interactions support its potential association with the target protein?

**3. Aim**

To evaluate the predicted binding pose and molecular interactions of quercetin with the ATP-binding domain of Escherichia coli DNA gyrase B using molecular docking.

**4. Objectives**
 
 a. Retrieve and inspect the experimentally determined structure of DNA gyrase B.
 
 b. Obtain the three-dimensional structure of quercetin from PubChem.
 
 c. Perform protein–ligand docking using Autodock Vina.
 
 d. Record and evaluate the predicted docking score and binding pose.
 
 e. Identify hydrogen bonds and other predicted interactions between quercetin and the protein.
 
**5. Biological Background**

**DNA Gyrase B**

DNA gyrase is a bacterial type II topoisomerase that introduces negative supercoils into DNA and helps manage DNA topology during essential cellular processes. The enzyme contains two principal subunits, GyrA and GyrB. GyrB contains an ATPase domain that binds and hydrolyses ATP, providing energy for the enzyme's catalytic cycle. Interference with DNA gyrase activity can disrupt bacterial DNA metabolism. Consequently, DNA gyrase is an established antibacterial drug target.

**Quercetin**

Quercetin is a naturally occurring flavonoid found in several fruits, vegetables, and other plant materials. It contains multiple hydroxyl groups and an aromatic ring system that may contribute to hydrogen bonding and other non-covalent interactions with proteins. In this project, quercetin will be investigated as a candidate ligand for DNA gyrase B. Its selection does not establish that it inhibits this particular protein. Any conclusions about target-specific inhibitory activity would require appropriate experimental evidence.

Molecular Docking

Molecular docking is a computational method used to predict how a small molecule may fit into a protein-binding pocket. Docking algorithms generate and evaluate possible ligand poses using a scoring function that estimates the favourability of predicted interactions. Docking results can help formulate hypotheses about protein–ligand recognition. However, docking scores are approximate computational estimates and should not be interpreted as experimentally measured binding free energies.

**6. Protein and Ligand Information**

**Protein Target**

 a. Protein: DNA gyrase B ATP-binding domain

 b. Organism: Escherichia coli

 c. PDB ID: 4KFG

 d. Structure source: RCSB Protein Data Bank

 e. Experimental method: X-ray crystallography

 f. Reported resolution: 1.60 Å

 g. Structure URL: https://www.rcsb.org/structure/4KFG

 h. The selected structure contains a co-crystallized small-molecule inhibitor.

**Ligand Information**

 a. Compound: Quercetin

 b. PubChem CID: 5280343

 c. Compound database: PubChem

 d. Structure URL: https://pubchem.ncbi.nlm.nih.gov/compound/5280343

 e. Chemical class: Flavonoid

 f. Ligand file: Three-dimensional SDF structure

7. Tools and Resources

The project uses molecular visualization software, ligand and protein preparation tools, molecular docking software, and a web-based protein–ligand interaction analysis platform.

 | Tool / Resource | Application |
|---|---|
| RCSB Protein Data Bank | Retrieve the protein structure |
| PubChem | Retrieve the 3D structure of quercetin |
| PyMOL | Visualize protein and ligand structures |
| AutoDockTools | Prepare protein and ligand files |
| AutoDock Vina | Perform molecular docking |
| ProteinPlus - PoseView | Visualize protein-ligand interactions |

## Methodology: Molecular Docking of Quercetin with DNA Gyrase B

### 1. Ligand Retrieval and Preparation

The 3D structure of quercetin was retrieved from the PubChem database in SDF format. The downloaded structure was opened in PyMOL and exported in PDB format for further preparation. The ligand was then imported into AutoDockTools (MGL Tools), prepared for docking, and saved as `quercetin.pdbqt`.

### 2. Protein Retrieval and Preparation

The crystal structure of the target protein, DNA gyrase B from *Escherichia coli* (PDB ID: 4KFG), was retrieved from the RCSB Protein Data Bank and saved as `4kfg.pdb`. The protein structure was loaded into AutoDockTools, and water molecules were removed. Hydrogen atoms and Kollman charges were added to prepare the receptor for docking. The prepared protein was subsequently saved in PDBQT format as `4kfg.pdbqt`.

### 3. Grid Box Configuration

The docking grid box was defined around the selected binding pocket of DNA gyrase B using AutoDockTools. The centre coordinates along the X, Y, and Z axes were determined according to the binding site, and the grid dimensions were selected to encompass the ligand-binding region.

The grid centre coordinates and box dimensions were entered into the AutoDock Vina configuration file, `config.txt`. The receptor and ligand filenames were specified as `4kfg.pdbqt` and `quercetin.pdbqt`, respectively. The exhaustiveness parameter was set to 8 to control the search effort during docking.

### 4. Molecular Docking Using AutoDock Vina

Molecular docking was performed using AutoDock Vina to predict the binding poses of quercetin within the selected binding pocket of DNA gyrase B. The docking was executed using the prepared receptor, ligand, and configuration files. The predicted binding poses were saved as `output.pdbqt`, while the docking scores and associated results were recorded in `log.txt`.

### 5. Analysis and Visualization of Docking Results

The docking log file was examined to identify the predicted binding affinities and rank the generated poses. The pose with the most negative predicted binding-affinity score was selected for further structural analysis, considering both its position within the binding pocket and its interactions with the protein.

The original protein structure was opened in PyMOL, and the predicted docked ligand pose was loaded for visualization. The protein and ligand were displayed using suitable structural representations and colours. The protein and selected docked ligand pose were then exported together as `4kfg-quercetin_docking.pdb`.

### 6. Protein–Ligand Interaction Analysis Using ProteinPlus

The combined protein–ligand structure, `4kfg-quercetin_docking.pdb`, was uploaded to the ProteinPlus web server and analysed using PoseView. The resulting two-dimensional interaction diagram was examined to identify hydrogen bonds, hydrophobic contacts, and other potential non-covalent interactions between quercetin and DNA gyrase B. These interactions were considered alongside the docking score to evaluate the predicted binding mode of the ligand.

## Results

### Molecular Docking Analysis

Molecular docking of quercetin with DNA gyrase B from *Escherichia coli* was performed using AutoDock Vina. Nine predicted binding poses were generated and ranked according to their predicted binding-affinity scores.

The highest-ranked pose, Mode 1, exhibited a predicted binding affinity of −9.3 kcal/mol, followed by Mode 2 at −8.6 kcal/mol and Mode 3 at −8.3 kcal/mol. The remaining poses showed scores ranging from −7.6 to −7.2 kcal/mol.

Mode 1 was selected as the primary candidate for further structural analysis because it had the most negative predicted binding-affinity score among the generated poses. Its RMSD lower and upper bounds were both 0.000 Å, as this pose served as the reference for comparing the alternative poses.

Overall, the docking results indicate a computationally predicted association between quercetin and the selected DNA gyrase B structure.

## Conclusion

The molecular docking analysis of quercetin with DNA gyrase B from *Escherichia coli* using AutoDock Vina identified a best-ranked binding pose with a predicted binding affinity of −9.3 kcal/mol. This score indicates a favourable predicted interaction according to the docking scoring function. Among the nine generated poses, Mode 1 exhibited the most negative binding-affinity score and was selected for further structural analysis.

These findings suggest that quercetin may have the potential to interact with DNA gyrase B. However, the predicted binding affinity alone cannot establish its inhibitory activity or antibacterial effectiveness. Further analysis of protein–ligand interactions, validation of the docking setup, and experimental studies are required to determine whether quercetin inhibits DNA gyrase B and contributes to antibacterial activity.



