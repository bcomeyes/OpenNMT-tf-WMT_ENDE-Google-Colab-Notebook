# OpenNMT-tf_WMT_ENDE Google Colab
This repo provides Google Colab notebooks that follow the example provided on the OpenNMT website (https://opennmt.net/Models-tf/) and more specifically this repo: https://github.com/OpenNMT/OpenNMT-tf/tree/master/scripts/wmt

Essentially, the notebooks help the new user get started and overcome some obstacles to doing the tutorial listed in the repo above, including installing an older version of TensorFlow along with implementing the necessary steps to utilize GPUs.  It provides a "ready to use out of the box" notebook(s) for new users who want to make use of Google Colab for learning how to use OpenNMT.

As a newcomer to OpenNMT, it took me a while to build this notebook from scratch due to a variety of concerns that arose when using Google Colab:  

Note: The reason a plural "notebook(s)" is used is to account for the different notebooks that accomplish similar but unique tasks (e.g., (a) build the SentencePiece model and vocab files, (b) to train the OpenNMT model and (c) to make inferences off a test set.  These cold of course be put in the same notebook but would be cumbersome and a bit unruly).

1) The notebook(s) connects with Google Drive for the data files (the data is included in this repo)
2) The notebook(s) downgrades TF (current Google Colab builds come installed with TF 2.15) since at the time of my project OpenNMT is compatible with TF builds up through 2.13.
3) The notebook(s) install cuda and cudnn so that GPUs can be utilized (this notebook utilzed a single A100 GPU which worked fine and ran to completion [i.e. no improvement on BLEU score after multiple evaluation cycles]).  There is a link at the top of the notebooks on getting started with multiple GPUs if you would like to try that.
4) The notebook(s) installs and builds the SentencePiece command line tools from C++ source (we won't use "pip install sentencepiece") for reasons explained in OpenNMT repo listed above.

More coming soon...
