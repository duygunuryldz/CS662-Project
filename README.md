# CS662-Project

In this repository, we provide the extra code that we have written for reproduction of the paper "[Backpack Language Models](https://arxiv.org/abs/2305.16765)".  

Since the naming conventions of Backpack model in the Huffing Face and the original perository of the paper is different, we adapt the code to work with HF model for Knowledge Manipulation (see ```knowledge_editing.ipynb```) and mitigation of gender bias (see ```gender_debias.ipynb```). Respective experiments and discussions are present in the report in Sections 4.2, 4.3, and 4.4.1. Each notebook file is self contained. 

## Environment Setup
```
conda create --name myenv
conda activate myenv
pip install torch
pip install transformers
pip install scipy
```

