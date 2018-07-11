FROM resin/raspberry-pi3-debian:jessie

RUN apt-get update && apt-get upgrade && apt-get install -yq \
   python sense-hat python-dev python-imaging raspberrypi-bootloader && \
   apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /usr/src/app

COPY . .

ENV INITSYSTEM on

CMD modprobe i2c-dev && python src/audio_analyzer_wav.py


#sudo apt-get update && sudo apt-get upgrade
#sudo apt-get install python-dev python-imaging python-smbus python-alsaaudio sense-hat python-numpy
