![image](./imgs/hand.gif)
# <img src="./imgs/icon.jpg" width="48">Colab-DeepMosaics

## Usage: Simply download `Colab-DeepMosaics.ipynb` and open it inside your Google Drive or click [here](https://colab.research.google.com/github/styler00dollar/Colab-DeepMosaics/blob/master/Colab-DeepMosaics.ipynb) and copy the file with "File > Save a copy to Drive..." into your Google Drive.

# Info about Colab
- If you can't open `Colab-DeepMosaics.ipynb` inside your Google Drive, try this [colab link](https://colab.research.google.com/github/styler00dollar/Colab-DeepMosaics/blob/master/Colab-DeepMosaics.ipynb) and save it to your Google Drive. The "open in Colab"-button can be missing in Google Drive, if that person never used Colab.
- Google Colab does assign a random GPU. It depends on luck.
- The Google Colab VM does have a maximum session length of 12 hours. Additionally there is a 30 minute timeout if you leave colab. The VM will be deleted after these timeouts.

### More example

origin | auto add mosaic |  auto clean mosaic  
:-:|:-:|:-:
![image](./imgs/example/lena.jpg) | ![image](./imgs/example/lena_add.jpg) | ![image](./imgs/example/lena_clean.jpg) 
![image](./imgs/example/youknow.png)  | ![image](./imgs/example/youknow_add.png) | ![image](./imgs/example/youknow_clean.png) 

* Compared with [DeepCreamPy](https://github.com/deeppomf/DeepCreamPy)

mosaic image | DeepCreamPy | ours  
:-:|:-:|:-:
![image](./imgs/example/face_a_mosaic.jpg) | ![image](./imgs/example/a_dcp.png) | ![image](./imgs/example/face_a_clean.jpg) 
![image](./imgs/example/face_b_mosaic.jpg) | ![image](./imgs/example/b_dcp.png) | ![image](./imgs/example/face_b_clean.jpg) 

* Style Transfer

origin | to Van Gogh | to winter
:-:|:-:|:-:
![image](./imgs/example/SZU.jpg) | ![image](./imgs/example/SZU_vangogh.jpg) | ![image](./imgs/example/SZU_summer2winter.jpg) 

An interesting example:[Ricardo Milos to cat](https://www.bilibili.com/video/BV1Q7411W7n6)

#### Get pre-trained models
You can download pre_trained models and put them into './pretrained_models'.<br>
[[Google Drive]](https://drive.google.com/open?id=1LTERcN33McoiztYEwBxMuRjjgxh4DEPs)  [[百度云,提取码1x0a]](https://pan.baidu.com/s/10rN3U3zd5TmfGpO_PEShqQ)<br>
[[Introduction to pre-trained models]](./docs/pre-trained_models_introduction.md)<br>

#### Simple example
* Add Mosaic (output media will save in './result')<br>
```bash
python3 deepmosaic.py --media_path ./imgs/ruoruo.jpg --model_path ./pretrained_models/mosaic/add_face.pth --use_gpu -1
```
* Clean Mosaic (output media will save in './result')<br>
```bash
python3 deepmosaic.py --media_path ./result/ruoruo_add.jpg --model_path ./pretrained_models/mosaic/clean_face_HD.pth --use_gpu -1
```
#### More parameters
If you want to test other image or video, please refer to this file.<br>
[[options_introduction.md]](./docs/options_introduction.md) <br>

## Acknowledgments
This code borrows heavily from [[pytorch-CycleGAN-and-pix2pix]](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) [[Pytorch-UNet]](https://github.com/milesial/Pytorch-UNet) [[pix2pixHD]](https://github.com/NVIDIA/pix2pixHD) [[BiSeNet]](https://github.com/ooooverflow/BiSeNet).

