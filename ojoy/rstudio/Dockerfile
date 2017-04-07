FROM rocker/rstudio:3.3.3		

RUN R -e 'install.packages("devtools"); \
          library(devtools); \
          install_version("ggplot2", "2.2.1", repos = "https://cloud.r-project.org/"); \
          install_version("dplyr", "0.5.0", repos = "https://cloud.r-project.org/"); \
          install_version("tidyr", "0.6.1", repos = "https://cloud.r-project.org/"); \
          install_version("data.table", "1.10.4", repos = "https://cloud.r-project.org/"); \
          install_version("shiny", "1.0.1", repos = "https://cloud.r-project.org/");'
