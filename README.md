# ArttnGAN

Most of the AttnGAN code is a reproduction of the [Pytorch implementation](https://github.com/taoxugit/AttnGAN) for reproducing AttnGAN results in the paper [AttnGAN: Fine-Grained Text to Image Generation with Attentional Generative Adversarial Networks](http://openaccess.thecvf.com/content_cvpr_2018/papers/Xu_AttnGAN_Fine-Grained_Text_CVPR_2018_paper.pdf) by Tao Xu, Pengchuan Zhang, Qiuyuan Huang, Han Zhang, Zhe Gan, Xiaolei Huang, Xiaodong He.


Some changes I added: 
- enabling the implementation for python3
- created different cofigs for the different artistic models I wanted to run
- added those pretrained models + their encoders (found in [DAMSMencoders](DAMSMenconders) & [models](models))
- made a jupyter notebook to run the GAN according to the different configs
- made a notebook for scraping images
- made a notebook for clustering 
- made a notebook for generating more captions for the input images

## How to use 
This implementation is done through jupyter notebooks, which have been run in Google Colab, accessing their free GPU.
- [prep_wikiart.ipynb](notebooks/prep_wikiart.ipynb) --> notebook for scraping and prepping the wikiart image dataset. 
- [prep_news.ipynb](notebooks/prep_news.ipynb) --> preps and scrapes the news data.
- [run_attngan.ipynb](notebooks/run_attngan.ipynb) --> notebook for running the models (before running, change the name of the desired `captions_xxx.pickle` file to `captions.pickle` & set the runtime type of Colab to GPU instead of CPU. Don’t clone the original AttnGAN repo if you’re using this one.)
- [ImageCaptioning.ipynb](notebooks/ImageCaptioning.ipynb) --> implements the [Image Captioning codebase from Ruotian Luo](https://github.com/ruotianluo/ImageCaptioning.pytorch) to generate more captions for the dataset.
- [filter_captions.ipynb](notebooks/filter_captions.ipynb) --> filters the named entities and the low-frequency words in the captions of the dataset. 
- [image_clustering.ipynb](notebooks/image_clustering.ipynb) --> clusters the images from the dataset. 
- [Survey_analysis.ipynb](notebooks/Survey_analysis.ipynb) --> contains the distribution plots etc. from the statistical analysis of the survey. 

The data that is supposed to be located in the different folders, can be scraped using the first two prep notebooks.
