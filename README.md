# DeepLearning-Project2
Usage:

For Training:
python -m torch.distributed.launch --nproc_per_node=<num of GPUs> main_dino.py --arch vit_small --data_path <image dataset path> --output_dir <output dir path>

For Visualization of Attention Maps:
python visualize_attention.py --image_path <imagePath> --pretrained_weights <.pth trained filePath> --patch_size 16 --output_dir <attention map output directory path>
