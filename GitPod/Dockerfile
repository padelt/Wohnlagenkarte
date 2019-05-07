FROM rocker/r-ver

RUN mkdir -p /home/gitpod/R/library \
    && R -e 'install.packages(c("jsonlite", "rlang", "shiny", "leaflet", "dplyr", "sp", "RSQLite", "DBI", "R.utils", "RColorBrewer", "scales", "lattice"), lib = "/home/gitpod/R/library")'

RUN DEBIAN_FRONTEND=noninteractive apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3-pip python3-venv && \
    apt-get clean
RUN python3 -m pip install dash dash_core_components dash_html_components flask flask_cors pandas pylint