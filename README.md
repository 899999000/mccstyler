# Multi-channel Correlated Diffusion for Text-Driven Artistic Style Transfer
Multi-channel Correlated Diffusion for Text-Driven Artistic Style Transfer

## Official Pytorch implementation of ["Multi-channel Correlated Diffusion for Text-Driven Artistic Style Transfer"]



![MAIN3_e2-min](https://github.com/899999000/mccstyler/blob/main/graph9.jpg)


## Abstract
> Text-driven image style transfer methods offer users intuitive control over artistic style, bypassing the need for reference style images. However, traditional approaches face challenges in maintaining content structure and achieving realistic stylization. In this paper, we present a novel multi-channel correlated diffusion model for text-driven artistic style transfer. By leveraging the CLIP model to guide the generation of learnable noise and introducing multi-channel correlation computation, together with the use of channel refinement to filter out redundant information generated by the multi-channel correlation computation, we overcome the destructive effect of noise on the image texture during the diffusion process. Furthermore, we design a threshold-constrained contrastive balance text-image matching loss to ensure the strong correlation between textual descriptions and stylized images. Experimental results demonstrate that our method outperforms state-of-the-art models, achieving outstanding image stylization while maintaining content structure and adhering closely to text style descriptions. Quantitative and qualitative evaluations confirm the effectiveness of our approach.
## Framework
![MAIN3_e2-min](https://github.com/899999000/mccstyler/blob/main/3.jpg)
The overall pipeline of our framework.
## Environment
```
conda create -n mccstyler python=3.9
conda activate mccstyler
pip3 install torch==1.9.0+cu111 torchvision==0.10.0+cu111 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html
```

## Install dependencies
```
pip install -e ./CLIP
pip install -r requirements.txt
```

## Pretrained models
[CC12M_cfg](https://the-eye.eu/public/AI/models/v-diffusion/cc12m_1_cfg.pth)
<br> Please download them and put them into the floder ./checkpoints/ <br> 

## Run
```
python main.py "./forest10.jpg" "A monet styler painting of tree" --output "./test/forest_test.jpg" -fs 0.8 -ws 0.2 -lc 3 --steps 200
```



## License
The codes and the pretrained model in this repository are under the MIT license as specified by the LICENSE file.<br>
