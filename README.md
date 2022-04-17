# scRNA Tutorial Rstudio and Jupyter
```
# How to create new conda environment
conda env create -n winuthayanon-lab -f winuthayanon-lab.yml
conda activate winuthayanon-lab

# How to add kernel
python -m ipykernel install --user --name winuthayanon-lab --display-name "winuthayanon-lab"

# How to remove kernel
jupyter kernelspec list
jupyter kernelspec remove -f winuthayanon-lab

# How to remove conda environment
conda env list
conda remove --name winuthayanon-lab --all

# How to export conda environment
conda env export -n winuthayanon-lab -f winuthayanon-lab.yml 

# Update all Python Packages on Linux
pip3 list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip3 install -U

# How to install and update R package

install.packages("dplyr")
install.packages("Seurat")
install.packages("patchwork")
# or 
R -e "install.packages('dplyr')"
R -e "install.packages('Seurat')"
R -e "install.packages('patchwork')"

# update all available packages
R -e "update.packages()"
# update, without prompts for permission/clarification
R -e "update.packages(ask = FALSE)"

# fix error
cat ~/.Renviron 
LD_LIBRARY_PATH="/opt/conda/lib:/usr/lib/R/lib:/usr/lib/x86_64-linux-gnu:/usr/lib/jvm/default-java/lib/server"
install.packages('hdf5r')
install.packages('rlang')

# or run R as root
Sys.setenv(LD_LIBRARY_PATH="/opt/conda/lib:/usr/lib/R/lib:/usr/lib/x86_64-linux-gnu:/usr/lib/jvm/default-java/lib/server")
install.packages('hdf5r')
install.packages('rlang')

# bash shell
export LD_LIBRARY_PATH="/opt/conda/lib:/usr/lib/R/lib:/usr/lib/x86_64-linux-gnu:/usr/lib/jvm/default-java/lib/server"
R -e "install.packages('hdf5r')"
R -e "install.packages('rlang')"

# How to remove package
remove.packages("name")
# How to find the package
find.package("name")
