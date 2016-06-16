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


By entering the code, ds.dims we can see the dimesnions of the data and their size
ds.data_vars gives the list of variables in the data and their types
ds.attrs gives the metadata for the dataset
We can pick any variable and see its attributes by appending the variable name to the data structure. Say for eg. ds.variable1
The valuse of the variable can also be seen by further appending values to the command. eg. ds.variable1.values
We can see the shape of the nd array associated with a particular variable by appending the name shape. eg. ds.varaiable1.shape
Once we know the shape of a variable, we can acess a particular value by mentioning its coordinates within its shape after the variable name. eg.print(ds.varaiable1[16][20][11][4].....)
We can also check for the extreme values of the variables. eg. np.max(ds.variable1)
We can calculated the statistics of the variable like mean, standard deviation etc.eg. np.mean(ds.variable1)
