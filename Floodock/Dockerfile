FROM continuumio/miniconda3

WORKDIR /home/flow

COPY ./app /home/flow/app
COPY ./docs /home/flow/docs
COPY ./tests /home/flow/tests


USER root

RUN apt-get update &&  apt-get install libgl1-mesa-glx -y

RUN DEBIAN_FRONTEND='noninteractive' apt-get install -y --no-install-recommends libxt6 -y

RUN conda install --quiet --yes -c conda-forge flopy && conda install --quiet --yes -c conda-forge gdal && conda install --quiet --yes vtk  && conda clean -tipsy

RUN pip install pandas scipy 

RUN DEBIAN_FRONTEND='noninteractive' dpkg --add-architecture i386 

RUN apt-get update && apt-get install wine32 || true # dpkg --add-architecture i386 && echo "yes" |
    
RUN apt-get update && apt-get install --no-install-recommends --assume-yes wine

WORKDIR /home/flow/app
