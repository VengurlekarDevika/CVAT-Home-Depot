**An instance segmentation is performed across the 10 different categories of Kitchen namely Sinks, Cabinets, Countertops, Cutting Boards, Dinnnerware, Skillets,
Mixing Bowls, Toaster Ovens, Wall Ovens and Garbage Disposals form the Home Depot Dataset. We used a pretrained COCO model for segmentation.

**Mask R-CNN was built using Faster R-CNN. While Faster R-CNN has 2 outputs for each candidate object, a class label and a bounding-box offset, 
Mask R-CNN is the addition of a third branch that outputs the object mask. The first stage consists of two networks, backbone (ResNet, VGG, Inception, etc) 
and region proposal network. These networks run once per image to give a set of region proposals. Region proposals are regions in the feature map which contain 
the object.The additional mask output is distinct from the class and box outputs, requiring the extraction of a much finer spatial layout of an object. In the second 
stage, the network predicts bounding boxes and object class for each of the proposed region obtained in stage1. Each proposed region can be of different size 
whereas fully connected layers in the networks always require fixed size vector to make predictions. Size of these proposed regions is fixed by using either 
RoI pool (which is very similar to MaxPooling) or RoIAlign method.

**Mask R-CNN is an extension of Faster R-CNN and works by adding a branch for predicting an object mask (Region of Interest) in parallel with the existing 
branch for bounding box recognition.

**ADVANTAGES OF MASK RCNN

**i. Simplicity: Mask R-CNN is simple to train. 
**ii. Performance: Mask R-CNN outperforms all existing, single-model entries on every task. 
**iii. Efficiency: The method is very efficient and adds only a small overhead to Faster R-CNN. 
**iv. Flexibility: Mask R-CNN is easy to generalize to other tasks. For example, it is possible to use Mask R-CNN for human pose estimation in the 
      same framework.


