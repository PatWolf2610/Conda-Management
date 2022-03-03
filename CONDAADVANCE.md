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
3. Update enviroment
* Update content in your yml file first
* conda env update --prefix path --file enviroment.yml --prune
```
conda env update --prefix F:\Anaconda3\envs\vegahvyml --file vegahvymlud.yml --prune
```

4. Enviroment variables