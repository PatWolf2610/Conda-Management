# CONDA ENVIROMENT MANAGEMENT

## ADVANCE MANAGEMENT

1. Prefix the location of eviroment
* conda create --prefix path
```
conda create --prefix F:\Anaconda3\envs\prefixvega
```
2. Create enviroment from yml file
* note: yml is a file contain the initial setup for an enviroment. Example:
```
name: vegahvyml 
channels:
	- default
dependencies:
	- depend1=version...
	- depend2=version...
prefix: /path/anaconda3/envs/....
```
* note: yml file of enviroment can be update to update enviroment
* create enviroment base on yml file
* note: move to the folder contain yml file first

```
conda env create -f vegahvyml.yml
```
3. Update enviroment (Not dome yet)
* Update content in your yml file first
* conda env update --prefix path --file enviroment.yml --prune
```
conda env update --prefix F:\Anaconda3\envs\vegahvyml --file vegahvymlud.yml --prune
```

4. Enviroment variables
* set a enviroment variable
* note: create and activate your enviroment first
* conda env config vars set my_var=value
```
conda env config vars set MYNAME=VIET
```
* remember to reactivate enviroment to apply change
```
conda activate vegahv
```
* To make sure variable set
```
conda env config vars list
```
* unset a variable
* conda env config vars unset my_var -n test-env
```
conda env config vars unset MYNAME -n test-env
```
5. Saving enviroment variable (for window) (Not understand yet)
* Enter the enviroment directory and create the subdirectories and files
* note: enter the enviroment directory first
``` 
mkdir .\etc\conda\activate.d
mkdir .\etc\conda\deactivate.d
type NUL > .\etc\conda\activate.d\env_vars.bat
type NUL > .\etc\conda\deactivate.d\env_vars.bat
```
* Edit .\etc\conda\activate.d\env_vars.bat as follow
* set MY_KEY='secret-key-value'
* set MY_FILE=C:\path\to\my\file
```
MY_KEY='secret-key-value'
MY_FILE=G:\python\VegaSeminar\PythonDotEnv
```
* set MY_KEY=
* set MY_FILE=
```
set MY_KEY=
set MY_FILE=
```
* When you run conda activate analytics, the environment variables MY_KEY and MY_FILE are set to the values you wrote into the file. When you run conda deactivate, those variables are erased.

6. Sharing an enviroment
* activate the enviroment need to export first
* then export the enviroment, that will create yml file
```
conda env export > environment.yml
```
* share the yml file to others