# Create A New Kernel/Environment in Jupyterhub/Jupyter Notebook (Uwaterloo)

The University of Waterloo provides the access to Jupyterhub where the students could login using their WatIAM and program based on online environments. 

**Issue**: some libraries cannot be sucessfully installed as the student has no permissions to write the path where the package will be installed.

**Cause**: the kernel/environment used to implement the python code is provided by the administrators and prohibited to write. You can simply use existing libraries.

**Solution**: create a new virtural kernel/environment to run the notebook/python.

1. Create a new virtual environment and activate it in Terminal:
```
virtualenv my_env
source my_env/bin/activate
```
2. Add the created environment to Jupyter
```
pip install ipykernel
python -m ipykernel install --user --name=my_env
```
Now you should be able to find my_env in your kernel.

See [Using Virtual Environments in Jupyter Notebook and Python](https://janakiev.com/blog/jupyter-virtual-envs/) for reference.
