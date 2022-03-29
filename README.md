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
