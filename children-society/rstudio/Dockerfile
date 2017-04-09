FROM rocker/rstudio:3.3.3

RUN R -e 'install.packages("devtools")'


RUN R -e 'library(devtools); \
          install_version("ggplot2", "2.2.1");'


RUN R -e 'library(devtools); \
          install_version("dplyr", "0.5.0");'

RUN R -e 'library(devtools); \
          install_version("tidyr", "0.6.1");'

RUN R -e 'library(devtools); \
          install_version("data.table", "1.10.4");'

RUN R -e 'library(devtools); \
          install_version("leaflet", "1.1.0");'

RUN R -e 'library(devtools); \
          install_version("shiny", "1.0.1", repos = "https://cloud.r-project.org/");'

RUN R -e 'library(devtools); \
          install_version("vcd", "1.4-3");'

RUN R -e 'library(devtools); \
          install_version("plotly", "4.5.2");'

RUN R -e 'install.packages("plyr")'
RUN R -e 'install.packages('tidyverse')'
RUN R -e 'install.packages('rmarkdown')'
RUN R -e 'install.packages('forecast')'
RUN R -e 'install.packages('rsqlite')'
RUN R -e 'install.packages('reshape2')'
RUN R -e 'install.packages('nycflights13')'
RUN R -e 'install.packages('caret')'
RUN R -e 'install.packages('rcurl')'
RUN R -e 'install.packages('crayon')'
RUN R -e 'install.packages('psych')'
RUN R -e 'install.packages('igraph')'
RUN R -e 'install.packages('tm')'
RUN R -e 'install.packages('magrittr')'
RUN R -e 'install.packages('stringr')'
RUN R -e 'install.packages('shinydashboard')'
RUN R -e 'install.packages('SnowballC')'
RUN R -e 'install.packages('NLP')'
RUN R -e 'install.packages('DT')'
RUN R -e 'install.packages('tidyverse')'
RUN R -e 'install.packages('RColorBrewer')'
RUN R -e 'install.packages('broom')'
RUN R -e 'install.packages('MASS')'
RUN R -e 'install.packages('randomforest')'
