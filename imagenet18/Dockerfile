FROM sanjeevm0/baseimage:18.04
MAINTAINER Sanjeev Mehrotra <sanjeevm@alumni.stanford.edu>

RUN conda install pytorch torchvision -c pytorch

RUN pip uninstall -y pillow
RUN CC="cc -mavx2" pip install -U --force-reinstall pillow-simd

RUN pip install tensorboardX
RUN pip install tqdm

