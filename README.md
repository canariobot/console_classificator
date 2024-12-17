# Description
I have created a consoles classificator by using a Convolutional Neural Network (CNN) as a master's practice. For this, I have created a Jupyter notebook with the code that should be executed and a dataset with 16 consoles (classes in this case): 
- game_boy
- nes
- nintendo_64
- nintendo_ds
- nintendo_game_cube
- nintendo_switch
- ps1
- ps2
- ps3
- ps4
- ps5
- wii
- xbox_360
- xbox_one
- xbox_series_s
- xbox_series_x
For the practice, we had to create and train our own CNN and use another pretrained model with Transfer Learning (TL), which generally improves the results. My CNN has 4 Convolutional Layers and 4 Fully Connected Layers, and for TL, I used the ResNet model. I trained the last Convolutional Layer and the Fully Connected Layers. My network doesn't yield as good results as the one trained with the ResNet model, so I recommend training with ResNet.

# Table of Contents
- [Installation](#installation)
- [Use](#use)

# Installation
1. Clone the repository:
```bash
git clone https://github.com/israhr12/console_classificator.git
```

2. Go to the repository directory:
```bash
cd console_classificator
```

3. Create a virtual environment (Conda, venv, etc). I used venv with Python 3.10.12 and my environment folder's name is env:
```bash
python -m venv env
```

4. Activate the environment:
```bash
source env/bin/activate
```

5. Install the dependencies:
```bash
pip install -r requirements.txt
```
# Use
Now you just need to run each cell in the order they appear in the conv_net.ipynb file. If you want to train and evaluate the ConvNet model, change the first parameter of the train() and evaluate_model_with_confusion_matrix functions to the model variable. On the other hand, if you want to train the ResNet model, replace the parameter with resnet. You also can change the number of ephocs by changing the parameter num_epochs.

Model ConvNet:
```bash
train(model, train_loader, num_epochs=10)
```
```bash
evaluate_model_with_confusion_matrix(model, test_loader)
```

Model ResNet:
```bash
train(resnet, train_loader, num_epochs=10)
```
```bash
evaluate_model_with_confusion_matrix(resnet, test_loader)
```

