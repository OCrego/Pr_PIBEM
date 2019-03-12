FROM mathlab/deal2lkit:latest
WORKDIR /home/dealii
RUN git clone https://github.com/OCrego/Pr_PIBEM.git
WORKDIR /home/dealii/Pr_PIBEM
RUN mkdir build
WORKDIR /home/dealii/Pr_PIBEM/build
RUN cmake ../
RUN make -j4
WORKDIR /home/dealii/Pr_PIBEM
RUN mkdir test_run
ENV PATH=".:${PATH}"
ENV PBEM_DIR="/home/dealii/Pr_PIBEM${PBEM_DIR}"
