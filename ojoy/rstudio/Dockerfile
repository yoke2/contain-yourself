FROM rocker/rstudio:3.3.3

#METHOD 1
#RUN wget http://cran.r-project.org/src/contrib/Archive/ggplot2/ggplot2_0.9.1.tar.gz
#RUN R CMD INSTALL ggplot2_0.9.1.tar.gz
#RUN R -e "install.packages("ggplot2",version = “2.2.1”,repos = "http://cran.us.r-project.org")"
#RUN R -e "install.packages("dplyr",version = “0.5.0”,repos = 'http://cran.us.r-project.org')"
#RUN R -e "install.packages("tidyr",version = “0.6.1”,repos = 'http://cran.us.r-project.org')"
#RUN R -e "install.packages("data.table",version = "1.10.4",repos = 'http://cran.us.r-project.org')"
#RUN R -e "install.packages("shiny",version = "1.0.1",repos = 'http://cran.us.r-project.org')"
#RUN R -e "install.packages(c('ggplot2', 'dplyr'), c('2.2.1', '0.5.0'))"
#RUN R -e 'install.versions(c("ggplot2", "dplyr", "tidyr", "data.table", "shiny"), c("2.2.1", "0.5.0", "0.6.1", "1.10.4", "1.0.1"))'

#METHOD 2 
#RUN require(devtools)
#RUN install_version("ggplot2", version = "0.9.1", repos = "http://cran.us.r-project.org")

#METHOD 3 --> THIS ACTUALLY WORKS BUT IS ASKING FOR SOME DEPENDENCY LIBRARIES
#RUN wget http://cran.r-project.org/src/contrib/Archive/ggplot2/ggplot2_0.9.1.tar.gz
#RUN R CMD INSTALL ggplot2_0.9.1.tar.gz

#TRY 4	
#RUN R -e 'install.packages(c('ggplot2', 'dplyr', 'tidyr', 'data.table', 'shiny'),c('2.2.1', '0.5.0', '0.6.1', '1.10.4', '1.0.1'))'

#TRY 5
#RUN R -e 'install.version('ggplot2',version='2.2.1',repos = 'http://cran.us.r-project.org')'

#TRY 6
#RUN echo 'install.versions(c('checkpoint', 'devtools'), c('0.3.3', '1.6.1'))'

