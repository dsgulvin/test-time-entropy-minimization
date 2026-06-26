Project Code for Test-time adaptation with TENT
Daniel Gulvin

This folder contains the models used for my TENT experiments on CIFAR-10-C, CIFAR-100-C and ImageNet-C.
All experiments are implemented inside the notebook gulvin_projectcode.ipynb, with saved outputs. I 
separated the two so you can just download the ipynb without the .pth files, since those are only needed
if you are rerunning the code. If you do rerun the code, the .ipynb and .pth files must be in the 
same directory.

This notebook includes dataset loading, baseline evals, TENT adaptation, entropy logging, and sequential corruption
experiments. All major results are already saved in the notebook outputs, so rerunning is optional.

Included 2 pretrained baseline models:
	- baseline_model.pth: ResNet-18 pretrained on ImageNet and fine-tuned final layer on CIFAR-10.
	- cifar_100baseline.pth: ResNet-118 pretrained on ImageNet and fine-tuned final layer on CIFAR-100.
	- Both models are baseline only and contain no TENT updates, I used them to load models before running TENT.

To rerun the experiments, you would need to download the datasets and place them in the correct folders indicated 
in the code. CIFAR-10-C was accessed from data/CIFAR-10-C as seen in get_cifar10c_loader. Cifar-100-C data was stored 
from the project directory at the path cifar100c/{corruption}. ImageNet-C was loaded from an imagenet_c folder which 
contained the downloaded ImageNet-C data for some corruptions at imagenet_c/{corruption}/{severity}.
