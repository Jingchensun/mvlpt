# Multitask Prompt Learning for Vision-Language Models

This repo contains the codebase of a series of research projects focused on adapting vision-language models like [CLIP](https://arxiv.org/abs/2103.00020) to downstream datasets via *multitask prompt learning*:

* [Multitask Vision-Language Prompt Tuning](https://arxiv.org/pdf/2211.11720.pdf)

## How to Install
This code is built on top of the toolbox [Dassl.pytorch](https://github.com/KaiyangZhou/Dassl.pytorch) and [CoOp](https://github.com/KaiyangZhou/CoOp) so you need to install the [`dassl`](https://github.com/KaiyangZhou/Dassl.pytorch#installation) and [PyTorch](https://pytorch.org/) environment first. After that, run `pip install -r requirements.txt` under `MVLPT/` to install a few more packages required by [CLIP](https://github.com/openai/CLIP) (this should be done when `dassl` is activated). The script for environment installation is in step 1.


#### Step 1 Install torch、Dassl、requirement.txt
```bash
bash scripts/install
```



#### Step 2: Follow [DATASETS.md](DATASETS.md) to install the datasets from [CoOp](https://github.com/KaiyangZhou/CoOp/tree/main/datasets) for multitask prompt initialization. Or run the following script: 
```bash
bash scripts/data.sh
```

#### Stpe 3: Run the Promp learning on 11 CoCP Datasets
```bash
bash scripts/mvlpt/main_mt_coopdata_cut.sh CoOp vit_b16 16 -1 1
```


## Models and Results

- The trained weights will saved on "output/ImageNet,Caltech101,Food101,StanfordCars,OxfordPets,OxfordFlowers,FGVCAircraft,SUN397,DescribableTextures,EuroSAT,UCF101". After trained, zip this folder and send it to me (you can use google drive).


## Citation
This code was borrow from the following papers

```bash
@article{shen2022mvlpt,
    title={Multitask Vision-Language Prompt Tuning},
    author = {Shen, Sheng and Yang, Shijia and Zhang, Tianjun and Zhai, Bohan and Gonzalez, Joseph E. and Keutzer, Kurt and Darrell, Trevor},
    journal={arXiv preprint arXiv:2211.11720},
    year={2022}
}
```
