FROM resin/raspberry-pi3-debian:jessie

RUN apt-get update && apt-get upgrade && apt-get install -yq \
   python sense-hat python-dev python-imaging python-smbus python-alsaaudio python-numpy raspberrypi-bootloader && \
   apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /usr/src/app

COPY . .

ENV INITSYSTEM on

CMD ["python", "/usr/src/app/src/audio_analyzer_wav.py"]


#sudo apt-get update && sudo apt-get upgrade
#sudo apt-get install python-dev python-imaging python-smbus python-alsaaudio sense-hat python-numpy
#modifica CMD con sintassi aggiornata ed estromissione i2c rimossa la seguente riga di comando:
#CMD modprobe i2c-dev && python src/audio_analyzer_wav.py