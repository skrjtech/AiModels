FROM nvidia/cuda:11.7.1-devel-ubuntu22.04

SHELL [ "/bin/bash", "-c" ]

RUN apt update && apt -y upgrade 
RUN apt-get update && apt-get -y upgrade 
RUN apt install -y sudo git curl

RUN bash <(curl -sSL https://raw.githubusercontent.com/skrjtech/linux-setup/main/installer/python.sh) 3.9.16
ENV PATH /usr/local/python/bin:$PATH
RUN pip install torch torchvision torchaudio
RUN pip install opencv-python-headless==4.5.5.64
RUN pip install PyQt5 
RUN apt install -y portaudio19-dev pulseaudio
RUN pip install sounddevice 
RUN pip install pyaudio 
RUN pip install numpy 
RUN pip install pandas 
RUN pip install matplotlib
RUN pip install scipy 
RUN pip install scikit-learn 
RUN pip install pyzmq

RUN apt install -y ffmpeg

CMD [ "/bin/bash" ]