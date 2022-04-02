# Decoupled Mask R-CNN for Solving Foreground Confusion
 
## Installation

- Ubuntu 16.04
- CUDA 11.1

```
conda create -n decoupled_mask_rcnn python=3.9 -y
source activate decoupled_mask_rcnn

conda install pytorch=1.10 cudatoolkit=11.1 torchvision -c pytorch

git clone https://github.com/stormstoutzhang/decoupled_mask_rcnn.git
python -m pip install -e decoupled_mask_rcnn
```

## Train
```
./tools/train_net.py --num-gpus 8 --config-file configs/COCO-InstanceSegmentation/decoupled_mask_rcnn_R_50_FPN_1x.yaml
```

## Inference
```
./tools/train_net.py --num-gpus 8 --config-file configs/COCO-InstanceSegmentation/decoupled_mask_rcnn_R_50_FPN_1x.yaml --eval-only MODEL.WEIGHTS /path/to/checkpoint_file
```

## Model Zoo
<table><tbody>
<!-- START TABLE -->
<!-- TABLE HEADER -->
<th valign="bottom">Method</th>
<th valign="bottom">Backbone</th>
<th valign="bottom">lr Sched</th>
<th valign="bottom">mask AP</th>
<th valign="bottom">download</th>
<!-- TABLE BODY -->
<tr>
<td align="center">Decoupled Mask R-CNN</td>
<td align="center">ResNet-50-FPN</td>
<td align="center">1x</td>
<td align="center">36.5</td>
<td align="center"><a href="https://pan.baidu.com/s/1ny7936ltxgSMXBEsFwdZVQ">model</td>
</tr>
</tbody></table>

```
Extraction Code: IVIP
```

## Acknowledgement
Thanks [**Detectron2**](https://github.com/facebookresearch/detectron2) team for the wonderful open source project!
