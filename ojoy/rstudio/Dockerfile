FROM rocker/rstudio

RUN R -e 'install.packages("devtools"); \
          library(devtools); \
          install_version("ggplot2", "2.2.1"); \
          install_version("dplyr", "0.5.0"); \
          install_version("tidyr", "0.6.1"); \
          install_version("data.table", "1.10.4"); \
          install_version("shiny", "1.0.1");'
