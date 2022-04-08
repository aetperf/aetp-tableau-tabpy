# README First

To work with the jupyternotebook (.ipyn) in an anaconda environment, you need to follow these instructions. 

## Creation of anaconda environment  
Download anaconda. 
Open anaconda prompt. 
To create and activate your environment enter the following lines: 

```
conda create -n myEnv python=3.9
conda activate myEnv
```

## Installation of the libraries
Once you are in your environment (it is activated), install the libraries with these command lines: 
```
 pip install jupyterlab
 pip install tabpy
 pip install pantab
 pip install matplotlib
 pip install ruptures
 pip install missigno
 pip install seaborn 
``` 

## Run the code
Start jupyter lab with the command: `jupyter lab`
In another anaconda prompt, start tabpy in your environment: `tabpy`
Then, run the notebook (shift+enter for every cell).

## Connect Tableau to Tabpy
To connect Tableau Desktop to Tabpy, go to Help > Settings and Performance > Manage Analytics Extension. 
Choose Tabpy.
Enter localhost in Hostname and 9004 in port, then save.

You can start using tabpy in Tableau. For example, to call the function get_slope create this calculated field: 
 ```
 SCRIPT_REAL("return tabpy.query('get_slope',_arg1, _arg2 )['response']", SUM([elapsed time]),MIN([Dt Deb Donnees]))
```

Check our article for more informations on how to detect outlying trends with Tabpy: https://www.architecture-performance.fr/ap_blog/using-tableau-to-detect-outlying-trends-and-ruptures/