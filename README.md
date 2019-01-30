# HDX-MD
This contains the analysis for the lipid-protein interaction from MD simulation on XylE in a DOPE bilayer.
The trajectory (traj.dcd) is provided along with the topology file system.psf.
There are two folders Contact and Density. Contact folder measures the average contact frequency of the Phospohorus atom of the DOPE headgroup with the protein atoms. Density measures the  lipid headgroup density at a particular z coordinate.
# Softwares required.
Analysis is performed using the tcl scripts. To perform the analysis user has to download VMD. VMD can be obtained here.
Python is also used for data processing and plot generation. User needs to install the following libraries:
NUMPY:
MATPLOTLIB:
# USAGE
# Contact calculation

cd  Contact.

Getting the average contact: vmd -dispdev -text -e measure_contact_memb.tcl .
Data formatting python count.py.
Data plotting python plot.py .

Density calculation 
cd Density
Getting the density: vmd64 -dispdev text -e measure-density.tcl 
Data plotting: python plot.py
