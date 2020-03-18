# COVID-19 Drug Descovery

De novo drug descovery for the novel coronavirus (COVID-19) through sequence generation using LSTM based RNNs. Inspired and started as a submission for the "Coronavirus Deep Learning Competition" put up by [Siraj Raval](https://www.twitter.com/sirajraval) and [Sage Health](https://www.sage-health.org/) for descovering novel ligand molecules that could eventually serve as inhibitors for the nCov-19, following the recent virus outbreak in Wuhan, Hubei China (December 2019) and the challenges behind coming up with a possible drug.

## Datasets
The SMILES dataset used for training and validation was the GDB-13 and Chembl dataset gotten from [here](http://gdb.unibe.ch/downloads/)

## Development Tools | Visualizing our Ligand Molecules and Calculating Binding Affinities
To visualize the 2D or 3D structures of the generated ligand molecules (currently in the SMILES format), we need to follow a couple of steps.

Firstly we need to covert the ligand from the SMILES format (.smi) to an AutoDock PDBQT format(.pdbqt), and we can do this using [Open Babel](http://openbabel.org/wiki/Main_Page), a chemical toolbox designed that speaks the many languages of chemical data. 

How we convert it is as such:
- We either paste the SMILES string in a text-area that is provided, or we choose the path assuming it's stored in a file.
- We then select the input format as a SMILES (.smi) and the output format as a AutoDock PDBQT (.pdbqt), while also deciding where you want your output to go (either printed or saved to a file). 
- Next we check the **GENERATE 3D coordinates** and click the **CONVERT** to do the conversion 

Next we need to load our AutoDock PDBQT (.pdbqt) file into [PyRx](https://pyrx.sourceforge.io/), a virtual screening software to finally view the 3D structure of our ligand. PyRx also uses [AutoDock Vina](http://vina.scripps.edu/) underneath. AutoDock Vina is an open-source program for doing molecular docking, and this becomes useful when we finally generate confidently, ligands with good chemical activities and we want to proceed to dock our ligand molecule with the virus genome to calculate their binding affinity.

## Contributions
Of course contributors are very much welcomed to support on this project. As this virus scales to a pandemic and is getting out of control more than ever now we need as much hands on deck to combat it. 

As a first contribution, you can fork this project, commit your name to the Contributors.md file and create your pull request, I shall be merging it as soon as I get the notification

Let's work collectively to build a community that will fight for and save humanity from this.