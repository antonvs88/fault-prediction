# fault-prediction
A machine learning model for fault prediction.

Sensor measurements are used to predict the failure of an expensive machine component.

<h4>Contents of repository</h4>

The repository includes codes for NSGA-II, simulation and a graphical user interface (GUI). The folders in the repository:

* *crowddynamics-simulation* contains files for running the GUI
* *crowddynamics-qtgui* contains the files that build the GUI
* *crowddynamics* contains all files for simulating the movement of a crowd
* *genetic algorithm* includes files to run the combined numerical simulation and NSGA-II
* *misc* includes files used in configuring the optimization problem

The numerical evacuation simulations are implemented in Python and the NSGA-II is implemented in Python and Bash that were run on a high performance computing cluster. It should be noted that the procedure is currently computationally very demanding.

See the *readme.txt* file in each folder for a more detailed overview of the codes in each folder.


<h4>Installing</h4>

Using Linux is recommended. The code works at least on Ubuntu 16.04. Do the following steps to install the repository:

* Install anaconda (https://docs.anaconda.com/anaconda/install/linux)
* Set environment variables `export PATH=/.../anaconda3/bin:$PATH` and `export PYTHONPATH=/.../anaconda3/bin:$PYTHONPATH`
* Clone the repository
* On terminal run `conda config --add channels conda-forge`
* Create a conda environment from the file *crowddynamics/environment.yml*
* On terminal run `source activate multiobj-guided-evac`
* On terminal, in folder *crowddynamics*, `run pip install --editable .`
* Change to folder *crowddynamics-qtgui* and run `pip install -r requirements.txt`
* Run `conda install pyqt=4`
* Run `conda install pyqtgraph==0.10.0`
* Run `conda install scikit-fmm==0.0.9`
* Run `pip install anytree==2.1.4`
* Run `pip install --editable .`

You might occur problems in installing some of the python packages. You can install these packages manually using `conda install` or `pip install`.
