
# HDX-MD
This contains the analysis for the lipid-protein interaction from MD simulation on XylE in a DOPE bilayer.
The trajectory (traj.dcd) is provided along with the topology file system.psf.
There are two folders Contact and Density. Contact folder measures the average contact frequency of the Phospohorus atom of the DOPE headgroup with the protein atoms. Density measures the  lipid headgroup density at a particular z coordinate.
# Softwares required.
# Git Installation and Download the source files
In order to follow the tutorial and to download the necessary files, users should install the git and use the command line version. In order to install git, please follow the instructions below:

https://www.atlassian.com/git/tutorials/install-git

After the git has been installed one needs to go to the directory where the analysis is to be done and download the files from command line
git clone https://github.com/mrinal-shekhar/HDX-MD.git
This downloads a folder HDX-MD
Analysis is performed using the tcl scripts. To perform the analysis user has to download VMD. VMD can be obtained here https://www.ks.uiuc.edu/Development/Download/download.cgi?PackageName=VMD.
Python is also used for data processing and plot generation. 

# linux/mac installation:
install latest version of Anaconda: https://www.anaconda.com/download/

install packages

pip install matplotlib

# Usage
# Contact calculation

cd  Contact

Getting the average contact: vmd -dispdev -text -e measure_contact_memb.tcl 

Data formatting: python count.py

Data plotting: python plot.py 

# Density calculation 

cd Density

Getting the density: vmd64 -dispdev text -e measure-density.tcl 

Data plotting: python plot.py

