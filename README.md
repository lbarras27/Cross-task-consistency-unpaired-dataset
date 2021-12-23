# Cross-task consistency with an unpaired dataset

## Information about the requirement needed for this project
You can create the same conda environment I used during this project. You just need to type: `conda env create -f environment.yml`. 
The frameworks used in this project are PyTorch, Torchvision, OpenCV and Matplotlib.

## Information about the files and folders
- `block.py` contains the base blocks for the deep networks (Convolutional blocks, Transposed Convolutional blocks, Residual blocks).
- `network.py` contains the implementation of the Generator architecture and of the Discriminator architecture.
- `model.py` contains the network I used in this project (more detail in the report)
- `dataloader.py` contains the class that handle and allow to load the data to be generated on the fly (Dataloader)
- `train.py` is the script that allows to train the network (more information in a next section)


## Getting the sample of the taskonomy dataset
The sample of the taskonomy dataset I used for this project can be download directly on this github page: https://github.com/alexsax/taskonomy-sample-model-1

## Training the model
Use this script: `python train.py --epoch 10 --lr 0.001 --output "directory_you_want_to_save_the_model_parameters" --batch_size 2 --percentage 0.2`
- `--epoch` is the number of iteration
- `--lr` is the learning rate used with Adam optimizer
- `--output` the directory you want to save your model parameters
- `--batch_size` is the batch size of the training
- `--percentage` is the percentage of your data you want to used to train (for example if you have 10k images and you have a percentage of 0.2, you will use 2k images to train.
