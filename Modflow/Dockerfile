FROM antoinecheronirisa/lmt-python-core:latest
USER root
RUN apt-get update && apt-get install libgl1-mesa-glx -y
RUN conda install --quiet --yes -c conda-forge flopy && conda install --quiet --yes -c conda-forge gdal && conda clean -tipsy
RUN apt-get update && apt-get install --no-install-recommends --assume-yes wine