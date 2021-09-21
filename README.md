# Implementation of GLKS

This is the implementation of GLKS proposed in "Thinking Globally, Acting Locally: Distantly Supervised Global-to-Local
Knowledge Selection for Background Based Conversation".

## 1. Download data from "https://github.com/nikitacs16/Holl-E" and use "Prepare_holl.py" to prepare the dataset.

+ (1) Download the Holl-E dataset, make sure "holl\raw_data-20190221T150829Z-001\raw_data\" contains the train, dev, test files.

+ (2) Change the configurations ("input_file", "version", "output_file") in "Prepare_holl.py" to prepare different versions of datasets.

+ (3) Download "glove.6B.300d" and put it in "holl/"

+ (4) Create a vocabulary file based on the training set of different versions in the format: "token \t token_frequency".

## 2. Change the configurations in "Run_GLKS.py" and run "python -m torch.distributed.launch --nproc_per_node=num_GPU Run_GLKS.py --mode='train/test'" to train or test models on different dataset versions.

Please cite the follwing paper paper if you use the code:

Author = {Ren, Pengjie and Chen, Zhumin and Monz, Christof and Ma, Jun and de Rijke, Maarten},



