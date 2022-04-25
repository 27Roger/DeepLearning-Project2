Abstract:
Auto-Segmentation automatically segments areas of interest in an image using self-supervised learning algorithms. 
DINO introduced the possibility of using Vision Transformers for Self-supervised learning. 
DINO has high accurate attention and fully unsupervised semantic segmentation capabilities. 
Trained ImageNet CNNs are strongly biased towards recognizing textures rather than shapes. 
Stylized ImageNet provides better performance for object detection thereby highlighting advantages of a shape-based representation. 
This paper explores the possibility of improving the auto-segmentation capabilities of Vision based Neural networks. 
We observed a lesser loss for the Stylized ImageNet as compared to ImageNet. However, we did not observe a better segmentation map for Stylized ImageNet.

Usage:

For Training:
python -m torch.distributed.launch --nproc_per_node=<num of GPUs> main_dino.py --arch vit_small --data_path <image dataset path> --output_dir <output dir path>

For Visualization of Attention Maps:
python visualize_attention.py --image_path <imagePath> --pretrained_weights <.pth trained filePath> --patch_size 16 --output_dir <attention map output directory path>
