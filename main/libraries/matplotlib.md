# Matplotlib
---

Matplotlib is one of the most popular Python packages used for data visualization. It is a cross-platform library for making 2D plots from data in arrays. It provides an object-oriented API that helps in embedding plots in applications using Python GUI toolkits such as PyQt, WxPythonotTkinter. It can be used in Python and IPython shells, Jupyter notebook and web application servers also.

#### Install Matplotlib 
~~~~
pip install matplotlib
~~~~

#### Import Matplotlib
~~~~
import matplotlib.pyplot as plt
~~~~

#### Create Title
~~~~
plt.title("Name")
~~~~

#### Create X and Y Labels
~~~~
plt.xlabel('Name')
plt.ylabel('Name')
~~~~
~~~~
plt.xlabel('Name', color='red')
plt.ylabel('Name', color='#ff0000')
~~~~

#### Create Plot
~~~~
plt.plot()
~~~~
~~~~
plt.plot(name_x, name_y)
~~~~
~~~~
plt.plot(name_x, name_y, color='#ff0000')
~~~~
~~~~
plt.plot(name_x, name_y, color='#ff0000', linestyle='--')
~~~~
~~~~
plt.plot(name_x, name_y, color='#ff0000', linestyle='--', label="Name")
~~~~

#### Add Labels in Plot
~~~~
plt.legend()
~~~~

#### Show Plot
~~~~
plt.show()
~~~~

#### Save Plot In Image
~~~~
plt.savefig('name.png')
~~~~
~~~~
plt.savefig('name.png', transparent = True) # Transparent Figure
~~~~

#### Close And Clear
~~~~
plt.cla() # Clear an axis
plt.clf() # Clear the entire figure
plt.close() # Close a window
~~~~