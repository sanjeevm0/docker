FROM sanjeevm0/baseimage:latest
MAINTAINER Sanjeev Mehrotra <sanjeevm@alumni.stanford.edu>

RUN conda install pytorch torchvision -c pytorch

RUN pip install git+https://github.com/fastai/fastai.git
#RUN git clone https://github.com/fastai/fastai.git /usr/local/fastai
#RUN cd /usr/local/fastai
#RUN conda env update
#RUN conda activate fastai

RUN pip uninstall -y pillow
RUN CC="cc -mavx2" pip install -U --force-reinstall pillow-simd
