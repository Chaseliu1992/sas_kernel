# SAS NBextensions


## Installing from PyPi
With the release of Jupyter 4.2 (sas_kernel version 1.2) you can now install and enable nbextensions in a much improved way.
To install and enable the showSASLog extension use the following command:
```
jupyter nbextension install --py sas_kernel.showSASLog
jupyter nbextension enable sas_kernel.showSASLog --py
```

To install and enable the theme extension use the following command:
```
jupyter nbextension install --py sas_kernel.theme
jupyter nbextension enable sas_kernel.theme --py
```

To verify the ebextensions you have installed use the following command:
```
jupyter nbextension list
```

If the extensions are correctly installed you will see output similar to this:
```
Known nbextensions:
  config dir: /root/.jupyter/nbconfig
    notebook section
      showSASLog/main  enabled 
      - Validating: OK
      theme/theme_selector  enabled 
      - Validating: OK
```

## Installing from a cloned repository
In your cloned repo you have a directory for each nbextension within the file structure as shown below:

```
sas_kernel
|
+-- showSASLog
+-- theme
```

Extensions are installed from the command line. 
To install it systemwide use the following command (you must be root or have sudo privileges). This assumes you're in the nbextensions directory otherwise adjust your path.
```
jupyter nbextension install ./showSASLog
```
Which should display something similar to this (if you have super user rights):

`copying showSASLog/main.js -> /usr/local/share/jupyter/nbextensions/main.js`


To install for the current user only use the following command. Again assumes you're in the nbextensions directory otherwise adjust your path.
```
jupyter nbextension install ./showSASLog --user
```
Which should display something similar to this (if you DO NOT have super user rights):

`copying showSASLog/main.js -> /home/sas/.local/share/jupyter/nbextensions/showSASLog/main.js`


Then enable the notebook extension with the following command:
```
jupyter nbextension enable showSASLog
``` 

To disable (not that you'd ever want to):

 `jupyter nbextension disable showSASLog`

## Example
There is a [notebook](../../notebook/loadSASExtensions.ipynb) that walks through the steps to install and enable the extensions

