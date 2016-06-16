# To open a netCDF on Jupyter
Install Jupyter notebook from www.jupyter.org
We can launch the notebook by entering "Jupyter Notebook" as a shell command
Jupyter opens in the default web browser of the OS
Jupyter notebook support around 40 programming languages. I have used ipython to code in it because it is a scripting language and is easy to understand  
On the top right corner of the dashboard you will have an option to launch a new notbook and the dropdown shows the list of programming languages available on the OS. I have opened a new notebook with ipython as the programming language
At the top of this notebook you can give a heading and the notebook can have markdowns written throughout out it to expplain the script of the code
Now beacuse a netCDF might nd arrays, working with pandas wouldn't be sufficient. So we have to install a library equivlent of pandas like "xarray" to work with netCDF files.
Once the xarray library is installed, we can either import the netCDF from local directory or from the internet. the function used to upen it is xarray.open_dataset()
Once the data is imported, you could see the number of dimensions, variables, coordinates and the attributes of the data by just calling the name of the data structure into which the file was assigned to, say for example "ds"
