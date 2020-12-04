# Reconnaissance-vocale-off-line-
Installation et example vosk, kaldi. 
Uilisation avec un micro usb MOVO model MC1000 (support alsa).

#1 Installation kaldi.
La reconnaissance vocal off line (vosk) se fait sur base de kaldi.
Installation kaldi  
------------------  
  git clone https://github.com/kaldi-asr/kaldi.git kaldi --origin upstream  
  cd kaldi  
Update  
------  
git pull  
  
Installation  
------------  
cd kaldi/tools  
Check independance : extras/check_dependencies.sh 
  
make TARGET=ARMV7     # pour Raspberry Pi4 (environ 1h de compilation) 
git clone https://github.com/xianyi/OpenBLAS  (peut se faire via le script extras/install_openblas.sh)
cd OpenBLAS 
make FC=gfortran  
--------------------------------------------  
A tester: 
  
git clone https://github.com/kaldi-asr/kaldi.git  
cd kaldi/tools  
check and install dependencies  
make  
cd ../src 
./configure --shared  
make depend 
make  
