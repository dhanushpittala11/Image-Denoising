# Image Denoising using Deep Learning

This is a Project on Denoising Images using Deep learning Techniques and comparing the performance with the traditional techniques. We used DnCNN Architecture, used variants of it to evaluate the performance of DnCNN.

## 1.Archiecture
The Architecture consists of three types of layers:
* **Conv+ReLU** :For the first layer, 64 filters of size 3×3×c are used to generate 64 feature maps, and rectified linear units(ReLU) are then utilized for nonlinearity. c represents thenumber of image channels.( for example: c=1forgrayimageandc=3forcolorimage.).
  
* **Conv+BN+ReLU** : for layers 2 to (D−1), 64 filters of size 3×3×64 are used, and batch normalization is added between convolution and ReLU. D is the depth of the architecture.

* **Conv**: for the last layer, c filters of size 3×3×64 are used to reconstruct the output.
  
### 1.1 DnCNN Architecture

![](DnCNN.png)

#### 1.1.1 Loss Function
Made use of Mean Squared Error Loss function.
![](MSE1.png)

#### 1.1.2 Training Loss

![](TrainingLoss_DnCNN.png)

#### 1.1.3 Results

![](DnCNN_img2.png)

### 1.2 Increased Depth DnCNN

We increased the depth of the same architecture by 3 more layers.I used the same loss function for this case.

#### 1.2.1 Training Loss

![](TrainingLoss_ID_DnCNN.png)

#### 1.2.2 Results

![](ID_DnCNN_img1.png)

### 1.3 Dilated DnCNN

Used Dilated Kernels instead usual kernels in the above increased Depth DnCNN Architecture. 

#### 1.3.1 Training Loss

![](TrainingLoss_Dilated_DnCNN.png)

#### 1.3.2 Results

![](ID_dilatedDnCNN_img1.png)

