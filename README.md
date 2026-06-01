<h2>TensorFlow-FlexUNet-Image-Segmentation-UDIAT-Breast-Ultrasound (2026/06/01)</h2>
Sarah T. Arai<br>
Software Laboratory antillia.com<br><br>
This is the first experiment of Image Segmentation for <b>UDIAT-Breast-Ultrasound (Benign and Malignant)</b> based on 
our <a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>), and a PNG
 <a href="https://drive.google.com/file/d/1rpI-qMOfi9v-O9ffBBsrtOHBUcHaIds-/view?usp=sharing">
Augmented-UDIAT-ImageMask-Dataset.zip</a>, which was derived by us from <br><br>
<a href="https://www.kaggle.com/datasets/sajidhussain4540/udiat-updated">
<b>UDIAT-updated</b>
</a> by Sajid Hussain.
<br><br>
<hr>
<b>Actual Image Segmentation for UDIAT Images</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to 
the ground truth masks.
<br><br>
<b>class-color-map = {Benign:green, Malignant:red}</b>
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/Benign_1045.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/Benign_1045.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/Benign_1045.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/deformed_alpha_1300_sigmoid_10_Malignant_1467.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/deformed_alpha_1300_sigmoid_10_Malignant_1467.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/deformed_alpha_1300_sigmoid_10_Malignant_1467.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/deformed_alpha_1300_sigmoid_9_Malignant_1474.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/deformed_alpha_1300_sigmoid_9_Malignant_1474.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/deformed_alpha_1300_sigmoid_9_Malignant_1474.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1. Dataset Citation</h3>
The dataset used here was derived from <br><br>
<a href="https://www.kaggle.com/datasets/sajidhussain4540/udiat-updated">
<b>UDIAT-updated</b>
</a> by Sajid Hussain.
<br>
<br>
For more information of Breaset Ultrasound Dataset B
, please refer to
<a href="https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/Breast_Ultrasound_DatasetB.md">
Breast Ultrasound Dataset B</a>
<br><br>

The following explanation was taken from the above <a href="https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/Breast_Ultrasound_DatasetB.md">
Breast Ultrasound Dataset B</a>.
<br><br>
<b>Dataset Information</b><br>
The Breast Ultrasound Dataset B is a collection specifically aimed at the analysis of breast ultrasound images, 
comprising a total of 163 images with detailed annotations. <br>
Among these images, 53 have been diagnosed as malignant, indicating the presence of breast cancer,
 while the remaining 110 have been identified as benign, showing non-cancerous breast conditions. <br>
 The composition of this dataset provides researchers with a unique resource for developing and 
 testing breast cancer detection algorithms. In particular, for the automated identification and 
 classification of breast lesions using deep learning and computer vision techniques, 
 the Breast Ultrasound Dataset B offers a range of challenging cases. <br>
 As these images are derived from real patient cases, they offer researchers the opportunity to gain 
 a deeper understanding of the characteristics of breast lesions, as well as supporting the validation 
 and improvement of various image processing and machine learning techniques. <br>
 The availability of the Breast Ultrasound Dataset B is of significant importance in advancing research in 
the field of automated breast cancer detection, especially in the context of a relative lack of public datasets.
<br>
<br>
<b>Citation</b><br>
<pre>
@article{yap2017automated,
  title={Automated breast ultrasound lesions detection using convolutional neural networks},
  author={Yap, Moi Hoon and Pons, Gerard and Marti, Joan and Ganau, Sergi and Sentis, Melcior and Zwiggelaar, Reyer and Davison, Adrian K and Marti, Robert},
  journal={IEEE journal of biomedical and health informatics},
  volume={22},
  number={4},
  pages={1218--1226},
  year={2017},
  publisher={IEEE}
</pre>
<br>
<b>License</b><br>
Unknown
<br>
<br>
<h3>
2 UDIAT ImageMask Dataset
</h3>
<h3>2.1 UDIAT ImageMask Dataset</h3>
 If you would like to train this UDIAT Segmentation model by yourself,
 please download the dataset from the google drive  
 <a href="https://drive.google.com/file/d/1rpI-qMOfi9v-O9ffBBsrtOHBUcHaIds-/view?usp=sharing">
Augmented-UDIAT-ImageMask-Dataset.zip</a> 
, expand the downloaded ImageMaskDataset and put it under <b>./dataset</b> folder to be
<br>
<pre>
./dataset
└─UDIAT
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
         ├─images
         └─masks
</pre>
<br>
<b>UDIAT Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/UDIAT/UDIAT_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is large enough to use for the
 training set of our segmentation model.
<br>
<br>
<h3>2.2 Derivation of UDIAT ImageMask Dataset</h3>
The folder of the original <b>UDIAT BC</b> dataset is the following.<br>
<pre>
./UDIAT BC
├─000001_Benign_image.png
├─000001_Benign_mask.png
...
├─malignant (210).png
└─malignant (210)_mask.png
</pre>
<b>Step 1</b><br>
We generated a master dataset from all pairs of images and their corresponding colorizied masks
 (Benign:green, Malignant:red)
 in <b>UDIAT BC</b> folder.
<br><br>
<b>Step 2</b><br>
 We generated our Augmented ImageMask dataset from the master by using the following image deformation tools.<br>
<a href="https://github.com/sarah-antillia/Image-Deformation-Tool">Image-Deformation-Tool</a><br>
<a href="https://github.com/sarah-antillia/Image-Distortion-Tool">Image-Distortion-Tool</a><br>
<br>
<h3>2.3 Train Sample Images and Masks</h3>

<b>Train sample images</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train sample masks</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/train_masks_sample.png" width="1024" height="auto">
<br>
<h3>
3 Train TensorFlowFlexUNet Model
</h3>
 We trained UDIAT TensorFlowFlexUNet Model by using the 
<a href="./projects/TensorFlowFlexUNet/UDIAT/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/UDIAT and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters = 16 </b> and large <b>base_kernels = (11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers = 8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
;You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 3
base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.05
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and <a href="./src/dice_coef_multiclass.py">"dice_coef_multiclass"</a>.<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b>RGB Color map</b><br>
Specifed rgb color map dict for UDIAT 1+2 classes.<br>
<pre>
[mask]
mask_datatyoe    = "categorized"
mask_file_format = ".png"
;UDIATrgb color map dict for 1+2 classes.
;                      Benign:green,  Malignant:red
rgb_map = {(0,0,0):0, (0, 255, 0):1, (255,0,0):2, }
</pre>
<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>
By using this callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
As shown below, early in the model training, the predicted masks from our UNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 23,24,25)</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>

<b>Epoch_change_inference output at ending (epoch 48,49,50)</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>

In this experiment, the training process was terminated at epoch 50.<br><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/train_console_output_at_epoch50.png" width="1024" height="auto"><br>
<br>

<a href="./projects/TensorFlowFlexUNet/UDIAT/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/UDIAT/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/UDIAT</b> folder,
and run the following bat file to evaluate TensorFlowUNet model for UDIAT.<br>
<pre>
>./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer_aug.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/evaluate_console_output_at_epoch50.png" width="1024" height="auto">
<br><br>Image-Segmentation-UDIAT

<a href="./projects/TensorFlowFlexUNet/UDIAT/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this <b>UDIAT/test</b> was low and dice_coef_multiclass high as shown below.
<br>
<pre>
categorical_crossentropy,0.0175
dice_coef_multiclass,0.9916
</pre>
<br>
<h3>
5 Inference
</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/UDIAT</b> folder<br>
,and run the following bat file to infer segmentation regions for images by the Trained-TensorFlowUNet model for UDIAT.<br>
<pre>
>./3.infer.bat
</pre>
This simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer_aug.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/mini_test_masks.png" width="1024" height="auto"><br>
<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/UDIAT/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks of UDIAT Images</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar 
to the ground truth masks.
<br><br>
<b>class-color-map = {Benign:green, Malignant:red}</b>
<br><br>
<table>
<tr>
<th>Image</th>
<th>Mask (ground_truth)</th>
<th>Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/Benign_1151.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/Benign_1151.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/Benign_1151.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/deformed_alpha_1300_sigmoid_8_Benign_1233.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/deformed_alpha_1300_sigmoid_8_Benign_1233.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/deformed_alpha_1300_sigmoid_8_Benign_1233.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/distorted_0.02_rsigma0.5_sigma40_Benign_1229.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/distorted_0.02_rsigma0.5_sigma40_Benign_1229.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/distorted_0.02_rsigma0.5_sigma40_Benign_1229.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/deformed_alpha_1300_sigmoid_9_Malignant_1487.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/deformed_alpha_1300_sigmoid_9_Malignant_1487.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/deformed_alpha_1300_sigmoid_9_Malignant_1487.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/distorted_0.03_rsigma0.5_sigma40_Malignant_1399.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/distorted_0.03_rsigma0.5_sigma40_Malignant_1399.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/distorted_0.03_rsigma0.5_sigma40_Malignant_1399.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/images/Malignant_1421.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test/masks/Malignant_1421.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/UDIAT/mini_test_output/Malignant_1421.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. TensorFlow-FlexUNet-Image-Segmentation-Breast-Ultrasound-Images</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Breast-Ultrasound-Images">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Breast-Ultrasound-Images</a>
<br><br>

<b>2. TensorFlow-FlexUNet-Image-Segmentation-Breast-Lesions-USG</b>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Breast-Lesions-USG">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Breast-Lesions-USG</a>
<br><br>
<b>3. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model</a>
<br><br>

