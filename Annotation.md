## DEXTR CUTTER


Deep Extreme Cut (DEXTR) is a simple matplotlib based annotation User Interface (UI) that can be used for extracting segmentation masks for images. The main 
advantage of using this tool is the speed of annotation even for complex objects the segmentation masks can be acquired by annotating only the four extreme 
points for that object. DEXTR obtains an object segmentation from its four extreme points namely the leftmost, the rightmost, top and bottom pixels. DEXTR 
outperforms other methods using extreme points or object proposals such as PASCAL and provides a better input to video object segmentation. Additionally, 
DEXTR can incorporate more points beyond the extreme ones which further refines the quality. DEXTR can also be used to obtain dense annotations to train 
supervised techniques.

## WORKING MECHANISM OF DEXTR


DEXTR is a deep learning based approach to obtain precise object segmentation in images and videos. To achieve the desired result, it follows a semiautomatic 
approach where usually user defined object extreme points are added as an extra channel to an image before it is sent as an input into a Convolutional Neural 
Network (CNN). The CNN learns to transform this information into a segmentation of an object that matches those extreme points. This approach is thus highly 
useful for guided segmentation such as the grabcut style, interactive segmentation, video object segmentation, and dense segmentation annotation. DEXTR 
requiresat least four markers for it to work. We create these markers by left clicking or by pressing "A" while the mouse pointer is hovering over one of 
these edges.As soon as the four markers are assigned, the DEXTR model will look for any object inside of those four markers. If the object selection within 
the four markers is not satisfactory then we can further continue to add points so as to get a desired output. However, we should know that at some point the 
results might be less than optimal. Markers can be moved by left clicking, holding and then dragging them to the desired position. We can also remove the
marker we placed last by pressing backspace. You can also select a marker that you want to delete by just striking it off with the cross sign which appears 
when we hover on the marker we want to delete or by first clicking on it and then pressing "Backspace". When we are satisfied with the selection, we can turn
it into an object by pressing “Enter” or by clicking the “Convert” button in the tool settings toolbar. After the task is completed which means when all the 
images are annotated we can download the dataset in any our desired formats. The desired formats are COCO, PASCAL VOC, YOLO, ImageNet, VGGFace, KITTI, CVAT, 
TFRecord, LabelMe, etc. The dataset can be downloaded in any desired format required by the user.


## ARCHITECTURE OF DEXTR



## SEGMENTATION FROM EXTREME POINTS


This is the type of segmentation used by DEXTR. Both the RGB image and the labeled extreme points are processed by the CNN to produce the segmented mask. 
Instance, Semantic, Video, and Interactive segmentation used this method of application to perform segmentation. The annotated extreme points are given as a 
guiding signal to the input of the network. We create a heatmap with activations in the regions of extreme points and then we center a 2D Gaussian around 
each of the points in order to create a single heatmap. The heatmap is concatenated with the RGB channels of the input image to form a 4-channel input for the
CNN. In order to focus on the object of interest, the input is cropped by the bounding box formed from the extreme point annotations. To include context on 
the resulting crop, we relax the tight bounding box by several pixels. After the preprocessing step that comes exclusively from the extreme clicks, the input 
consists of an RGB crop including an object plus its extreme points. In our model Home Depot, we have used segmentation from the extreme points so as to 
label the different objects in the category Kitchen.


## APPLICATIONS OF DEXTR


## ANNOTATIONS


For semi-automatic annotation, a tool called DEXTR is provided. It works by selecting some extreme points of an object after which the complete segmentation 
is derived. The common annotation pipeline for segmentation can  be assisted by DEXTR. In this framework instead of detailed polygon labels, the workload of 
the annotator is reduced to only providing the extreme points of an object and DEXTR produces the desired segmentation based on those extreme points. In this 
pipeline, the labelling cost is reduced by a factor of 10. The quality of the produced masks are validated when used to train a semantic segmentation 
algorithm. 

## INTERACTIVE OBJECT SEGMENTATION

The pipeline of DEXTR can also be used in the frame of interactive segmentation. A previous work has been done where the user labels the extreme points of an
object but is nevertheless not satisfied with the obtained results. The natural thing to do in such case is to annotate an extra point but not the extreme 
point in the region that segmentation fails and expect for a refined result. Given the nature of extreme points, we expect that the extra point also lies in 
the boundary of the object. To simulate such behavior, we first train DEXTR on a first split of a training set of images using the 4 extreme points as input. 
For the extra point, we infer on an image of the second split of the training set and compute the accuracy of its segmentation. If the segmentation is 
accurate then the image is excluded from further processing. In the opposite case, we select a fifth point in the erroneous area. 

## VIDEO OBJECT SEGMENTATION 

DEXTR can also improve the pipeline of video object segmentation. If a semi-supervised setting is considered then the methods use one or more masks as inputs
to produce the segmentation of the whole video. In a study working on video object segmentation, it was noted that they wanted to replace the costly per 
pixel annotation masks by the masks produced by their algorithm after the user has selected the extreme points of a certain object and retrain strongly 
supervised state-of-the-art video segmentation architectures.




## The link to my CVAT PROJECT which includes 10 categories containing 1000 images. Each category contains 100 images each
 
## Project: https://app.cvat.ai/projects?page=1
## Tasks: https://app.cvat.ai/tasks?page=1
