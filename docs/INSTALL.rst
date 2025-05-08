Installation
------------

### Requirements:
*   Python >= 3.9

#### Step 1: Create a virtual environment
```commandline
conda create -n venv_chronix2grid python=3.9
conda activate venv chronix2grid
```

#### Step 2 (first option): Install from source
```commandline
mkdir c2g_test
cd c2g_test
git clone https://github.com/Grid2op/chronix2grid.git
cd chronix2grid
pip install -U .
```

#### Step 2 (second option): Install from pypi
```commandline
source venv_chronix2grid/bin/activate
pip install Chronix2Grid
```

#### Step 3: Install library requirements
```commandline
pip install -r requirements_test.txt
```


Additional install required for dispatch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A backend for dispatch has been implemented with PyPSA 

 ```commandline
pip install -U pypsa
```
Note: Currently, HIGHS is used as the Optimal Power Flow (OPF) solver due to its fast computation. If you prefer the CBC solver, please install it from: [https://projects.coin-or.org/Cbc](https://github.com/coin-or/Cbc/releases)

[Optional] Compile and output the sphinx doc (this documentation)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Run
``./docs/make.bat html``
