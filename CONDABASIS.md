# ANACONDA ENVIROMENT MANAGEMENT

## BASIC MANAGEMENT
1. Create a new enviroment
* conda create -n envname python=version
```
conda create -n vegahv python=3.8.11
```
2. Activate(switch) enviroment
* conda activate envname
```
conda activate vegahv
```
* If use only conda activate, the enviroment will switch to base(default)
3. List enviroment
```
conda env list
```
4. List package in current enviroment
```
conda list
```
5. Clone the enviroment
* conda create --name myclone --clone myenv
```
conda create --name vegahvclone --clone vegahv
```
6. Install package
* conda install -c conda-forge package_name
```
conda install -c conda-forge python-dotenv
```
* Recommend Google search for: pakage_name anaconda then copy the command.
* Note: conda install often addition install many side package relate to main package, pip install usually install only main packages and very few addition package

7. Remove enviroment
* conda env remove --name envname
```
conda env remove --name vegahvclone
```
8. History and restore
* View log changing history of current enviroment
* See the log with related REVNUM
```
conda list --revisions
```
* Restore enviroment history
* Choose the wanting REVNUM in log list
```
conda install --revision=REVNUM
```

