# aisd-deforestation-cw2

---
## Project Overview

This project replicate the Attention U-Net model from An Attention-Based U-Net for Detecting Deforestation and adapts it to a new, Chinese context using the LoveDA dataset for building footprint segmentation.
The work consists of two main components:

Replication – replicating the original model architecture and evaluation pipeline on the Amazon forest datasets.

Localization – modifying the model to operate on RGB LoveDA imagery and perform binary building segmentation.

## Replication
The original Attention U-Net was reimplemented and trained following the procedures of the paper. Performance falls within the ±5%. 


## Adaptation to the Chinese Context
The model was modified to:
- Accept RGB inputs from the LoveDA dataset  
- Output binary building masks  
- Use BCE + Dice loss  
- Employ a tf.data pipeline with light augmentation  

Trained on LoveDA’s training split and evaluated on the validation set.


## Dataset: LoveDA
- 5,987 RGB images (1024×1024) from Nanjing, Wuhan, and Changzhou  
- Multi-class semantic masks → building class extracted for binary segmentation    
- Contains no personal or sensitive information  
Links to Dataset: https://zenodo.org/records/5706578


## SDG Relevance
- **SDG 11:** Supports urban planning and land-use monitoring.
- **SDG 15:** Helps monitor land-use change.
  
