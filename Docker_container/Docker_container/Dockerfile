# cd /mnt/c/Users/shravan.balasubr/Desktop/MODULES/'Module 4'/Assignment_4.2/Docker_container
# docker build -t my_project .
# docker run -it <image ID>

FROM continuumio/miniconda3

WORKDIR /home/shravan.balasubr

COPY housing_price_prediction .

RUN conda env create --file env.yml
RUN conda run -n mle-dev pip install -e .
RUN conda run -n mle-dev python3 housing_packaged/main.py
RUN conda run -n mle-dev pytest