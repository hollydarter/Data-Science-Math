# Wardrobe Wizard Project - MAP 2192 - Holly Darter

## Overview

Welcome to the Wardrobe Wizard Project, part of the MAP 2192 course led by Holly Darter. This project focuses on experiment tracking, PDF manipulation, image conversion, and PyTorch visualization.

## Installation

To set up the necessary environment, run the following commands:

```bash
%%capture
!pip install wandb
!apt-get install poppler-utils
!pip install pdf2image
!pip install flashtorch

Make sure to import the required Python libraries:

python
Copy code
import requests
from pdf2image import convert_from_path
import matplotlib.pyplot as plt
import numpy as np
import torch
from torchvision import *
import wandb as wb
