# PannelAppDB
PanelAppDB
============
PanelAppDB is a tool to search and store gene panel information for genetic tests included in the National Genomic Testing Directory.

- For help please use `-h` command

Functionality
---------------
Functionality provided by PanelAppDB include:
- Search for gene panel information by R code
- Generate BED file for gene panels
- Search for gene panels used for specific patients

ReadTheDocs documentation available at: https://softeng-module.readthedocs.io/en/latest/ 

## Install via conda
```bash
git clone https://github.com/Fr3dMer/softeng_module.git
conda env create -n PanelAppDB --file environment.yml
conda activate PanelAppDB
mkdir db
```

## Install via pip
- This section has been added to satisfy the rebric 
```bash
git clone https://github.com/Fr3dMer/softeng_module.git
# Recommend creating venv or conda environment and activating it before carrying out this step
pip install -r docs/requirements.txt
mkdir db
```
## Running script localy using conda environment above in normal mode
```bash
conda activate PanelAppDB
mkdir db
python PanelAppDB.py -r R45 -g 123 -pid 123 -sid 456 -f 'db/'
```
## Building and running script inside container 
```bash
sudo docker build --rm -t "panel_app_db" .
sudo docker run --rm panel_app_db <PARAMS HERE>
# example
sudo docker run --rm panel_app_db -p 3 -g 123 -pid 123 -sid 456 -d 
```

## Running script localy using conda environment above in debug mode
```bash
conda activate PanelAppDB
mkdir db
python PanelAppDB.py -r R45 -g 123 -pid 123 -sid 456 -d -f 'db/'
```



## Tests
```bash
pytest test/
```



## Structure of app
![flow chart showing structure of app](docs/Flowchart.png)

