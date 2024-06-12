# OpenNMT-tf wmt_ende Google Colab
This repo provides a Google Colab notebook that follows the example provided on the OpenNMT website (https://opennmt.net/Models-tf/) and more specifically this repo: https://github.com/OpenNMT/OpenNMT-tf/tree/master/scripts/wmt

Essentially, the notebook helps the new user get started and overcome some obstacles to doing the tutorial listed in the repo above if you want to use Google Colab (e.g., so that you can take advantage of GPUs), including installing an older version of TensorFlow along with implementing the necessary steps to utilize GPUs.  It provides a "ready to use out of the box" notebook for new users who want to make use of Google Colab for learning how to use OpenNMT.

As a newcomer to OpenNMT, it took me a while to build this notebook from scratch due to a variety of concerns that arose when using Google Colab:  

1) The notebook connects with Google Drive for the data files (you'll need to edit the "cd" --change directory--locations to match your set up. 
2) The notebook downgrades TF (current Google Colab builds come installed with TF 2.15) since at the time of my project OpenNMT is compatible with TF builds up through 2.13.
3) The notebook install cuda and cudnn components so that GPUs can be utilized (this notebook utilzed a single A100 GPU which worked fine and ran to completion [i.e. no improvement on BLEU score after multiple evaluation cycles]).  There is a link at the top of the notebooks on getting started with multiple GPUs if you would like to try that.

Steps to use this notebook with Google Drive and Google Colab:
1) Create a folder on Google Drive (e.g., wmt_ende)
2) Change directory so that you are inside wmt_ende
3) Create two more folders: config and data
4) Inside config directory, place the .yml file
5) Inside data directory, place the following files wmt_EN_DE/data:
train.en,
train.de,
valid.en,
valid.de,
wmtende.model,
wmtendevocab
  You can either tokenize these files yourself with SentencePiece or get the files from the tar.gz file "wmt_ende_sp.tar.gz" from the data hyperlink at OpenNMT's website https://s3.amazonaws.com/opennmt-trainingdata/wmt_ende_sp.tar.gz  and put the six files into the data directory.
(Note: See https://github.com/OpenNMT/OpenNMT-tf/tree/master/scripts/wmt for more info on this part)
7) Open and run the notebook: wmt_EN_DE_NMT.ipynb


