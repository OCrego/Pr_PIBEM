FROM mathlab/deal2lkit:latest
WORKDIR /home/dealii
RUN git clone --branch spheroid_cad https://github.com/nicola-giuliani/pi-BEM.git
WORKDIR /home/dealii/pi-BEM
RUN mkdir build
WORKDIR /home/dealii/pi-BEM/build
RUN cmake ../
RUN make -j4
WORKDIR /home/dealii/pi-BEM
RUN mkdir test_run
ENV PATH=".:${PATH}"
ENV PBEM_DIR="/home/dealii/pi-BEM${PBEM_DIR}"
