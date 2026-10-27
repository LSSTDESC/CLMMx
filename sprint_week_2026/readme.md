# Readme

We store the scripts here for the Sprint Week 2026.

## [Oct 26, 2026]

### Installing CLMM on RSP

Run the code below:

```
pip install clmm
pip install pyccl
pip install qp-prob
```

Using `conda` may work, but it is under the lsst stack and may cause some issue.

You can test the installation by running `import clmm` via `python3` in the terminal or in a Jupyter notebook. The current version is 1.16.10.

To use the latest version of the code, use
```
git clone https://github.com/LSSTDESC/CLMM.git
```

Then
```
import sys
sys.path.insert(0, "path_to_CLMM")
  
import clmm
print(clmm.__version__, clmm.__file__)   # should print 1.18.0 (or the latest one) and a path inside your clone
```

Or equivalently
```
cd path_to_CLMM
pip uninstall clmm          # remove the 1.16.10 copy, if present
pip install -e .            # links to your clone and installs the dependencies
pip install pyccl           # or another backend
pip install qp-prob
```

This will use the current branch.  Run `git pull` to get the newest `main`.
