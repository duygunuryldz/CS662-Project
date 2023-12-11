# CS662-Project

In this repository, we provide the extra code that we have written for reproduction of the paper "[Backpack Language Models](https://arxiv.org/abs/2305.16765)".  

Since the naming conventions of Backpack model in the Huffing Face and the original perository of the paper is different, we adapt the code to work with HF model for Knowledge Manipulation (see ```knowledge_editing.ipynb```) and mitigation of gender bias (see ```gender_debias.ipynb```). Respective experiments and discussions are present in the report in Sections 4.2, 4.3, and 4.4.1. Each notebook file is self contained. 

## Requirements Run Notebooks
```
torch
transformers
scipy
```
## Notes for Running the Original Repo
Run
```
pip install -r requirements.txt
```
to install all dependencies.

CUDA version strictly relies on ```nvcc --version``` of 11.7. If you have ```nvidia-smi``` greater than 11.7 but ```nvcc``` is not consistent, try
```
conda install -c "nvidia/label/cuda-11.7.0" cuda-toolkit
```

Then, run the [orginal repository of the Backpack models](https://github.com/john-hewitt/backpacks-flash-attn).





