# CS598 Final Project Team 69

Video link: https://drive.google.com/file/d/1Tk_DScRyy7Hsy3WkNswCoYiOEMgSxK1Q/view?usp=sharing

The project is based on the GLIP project, so please first setup the environment for the GLIP model following this instruction. Please make sure you download the GLIP-T Model weight here and put it under the MODEL/ path. Next, please clone this repository and continue the installation guide in the next section.

Installation
```
pip install -r requirements.txt
```
Configuration Files

We follow the config file format used in the GLIP project. Please refer to the sample config file we provided to create your own config file. Note: The DATASETS.CAPTION_PROMPT content is ignore by our code, as our code use the automatically generated code instead of user inputted prompt.

To get the MLM method generated prompts
```
python make_autopromptsv2.py --dataset 'kvasir' \
      --cls_names 'polyp' \
      --vqa_names 'bump'\
      --mode 'lama'\
      --real_cls_names 'bump'
```

To get the OFA method generated prompts
```
%run make_autopromptsv2.py --dataset 'kvasir' \
      --cls_names 'polyp' \
      --vqa_names 'bump'\
      --mode 'hybrid'\
      --real_cls_names 'bump'
```


