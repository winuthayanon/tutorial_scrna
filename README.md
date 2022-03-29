# scRNA Tutorial Rstudio and Jupyter
How to install and update R package

```
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
# How to remove package
remove.packages("name")
# How to find the package
find.package("name")
