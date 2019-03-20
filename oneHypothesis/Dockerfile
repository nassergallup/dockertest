###### Dockerfile #######
FROM jrnold/rstan

# Set the working directory to /app
#RUN mkdir /home/rstudio

# Copy the current directory contents into the container at /app
COPY NGS2_WITNESS_Cycle2_Notebook__1_.Rmd /home/rstudio/

RUN R -e "options(repos = \
  list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-02-06/')); \
  install.packages('pacman', dependencies=TRUE); \
  install.packages('formatR', dependencies=TRUE); \
  install.packages('Hmisc', dependencies=TRUE); \
  install.packages('bridgesampling', dependencies=TRUE); \
  install.packages('recipes', dependencies=TRUE); \
  install.packages('caret', dependencies=TRUE); \
  install.packages('pROC', dependencies=TRUE); \
  install.packages('randomForest', dependencies=TRUE)"

#RUN echo "pacman::p_load(Hmisc, bridgesampling, caret, pROC, randomForest)\n" >> /home/rstudio/.Rprofile

# These are installed as part of the notebook: 
# Hmisc
# bridgesampling
# caret
# ERROR: dependency ‘recipes’ is not available for package ‘caret’
# pROC
# randomForest