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

After established a conda environment ```flenv``` in [orginal repository of the Backpack models](https://github.com/john-hewitt/backpacks-flash-attn)

Our ```requirements.txt``` contains complete dependency, run
```
pip install -r requirements.txt
```


CUDA version strictly relies on ```nvcc --version``` of 11.7. If you have ```nvidia-smi``` greater than 11.7 but ```nvcc``` is not consistent, try
```
conda install -c "nvidia/label/cuda-11.7.0" cuda-toolkit
```


Then, run the [orginal repository of the Backpack models](https://github.com/john-hewitt/backpacks-flash-attn) for training from scratch and evaluation given model checkpoints.

Our pre-trained models can be downloaded: 
| Model  | Links |
| ------------- | ------------- |
| Backpack-micro| [link](https://drive.google.com/file/d/1j9f9c8Voi8rQCEgT4Q-bVBljQ5TIv9MK/view?usp=sharing)    | 
| Backpack-small | [link](https://drive.google.com/file/d/1ow1TnxukMpjLZBQwPvk7f_FqQCNjowwv/view?usp=sharing)    |

### Ablation
If you want to train a model without tie_weight, comment out ```self.tie_weights()``` at line 35 in ```~/backpacks-flash-attn/training/src/models/backpack.py```
We also provide the pre-trained ```Backpack-micro-without_tie_weight``` model below.

| Ablation| |
| ------------- | ------------- |
| Backpack-micro-without_tie_weight | [link](https://drive.google.com/file/d/1XrYuug6hx4sJO7YnNfX-QA_DSjAiavNk/view?usp=sharing)|

### Additional datasets
If you want to evaluate the additional datasets mentioned in paper, the task names are ```boolq,cb,copa,multirc,record,wic,wsc,openbookqa,piqa,triviaqa,truthfulqa_mc,logiqa,headqa_en,pubmedqa```. You can modify ```do_all.sh``` file as mentioned in evaluation part.

Before evaluating on ```truthfulqa_mc```, make sure run 
```
pip install bleurt@https://github.com/google-research/bleurt/archive/b610120347ef22b494b6d69b4316e303f5932516.zip#egg=bleurt
```

