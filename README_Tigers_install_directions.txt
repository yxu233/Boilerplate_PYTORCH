Compute canada:
(1) Create virtual environment: - this will become main folder you work in
module load python/3.6   ### might be at 3.7 at this point
virtualenv --no-download pytorch
source pytorch/bin/activate        ### this activates the virtual environment anytime you want to use it

(2) Installation of python packages (within virtual environment):
	pip install matplotlib scipy scikit-image pillow numpy natsort opencv-python keras pandas skan Cython sklearn numba torchio

### other side notes:
	# ***installing sklearn requires Cython!
	# (SKAN ==> requires pandas, numba... ==> DOES NOT WORK ON BELUGA, numba is broken)
	# *** pip install tifffile NO LONGER WORKS??? (or does it?)

(3) Job submission script template:
#!/bin/bash
#SBATCH --gres=gpu:1   # requests GPU "generic resource"
#SBATCH --cpus-per-task=10 # max CPU cores per GPU request (6 on Cedar, 16 on Graham).
#SBATCH --mem=80000M   # memory per node (in mbs)
#SBATCH --time=02-00:00 # time (DD-HH:MM) OR (hh:mm:ss) format
#SBATCH --output=%N-%j.out # %N for node name, %j for jobID

module load cuda cudnn python/3.5   # load python and then tensorflow
source pytorch/bin/activate
python ./filename.py


###############################################################################################################

Graphics card drivers and compatability (may be tricky with windows)
# CUDA Toolkit ==> needs VIsual studio (base package sufficient???)
# CuDnn SDK ==> 
# Ignore step about putting cudnn with Visual Studio

###############################################################################################################

Install for Pytorch (***on compute canada AND home computer)
 (1) Go to website and get the custom install command that should look something like this: conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
          
     torch.__version__ to check install in Python
     
     ***For uninstall:
     conda install pytorch torchvision cudatoolkit=10.2 -c pytorch  
     
***if gives error about pyqt5, need to
pip uninstall pyqt5
pip install pyqt5==5.12.0
then retry


