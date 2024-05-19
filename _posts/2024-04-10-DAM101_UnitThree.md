---
Title: DAM101 UnitThree
categories: [DAM101, UnitThree]
tags: [DAM101]
---
## Topic : Convolution Neural Network

A Convolutional Neural Network (CNN) is a type of deep learning neural network that is well-suited for image and video analysis. CNNs use a series of convolution and pooling layers to extract features from images and videos, and then use these features to classify or detect objects or scenes.

### CNN architecture

Convolutional Neural Network consists of multiple layers like the input layer, Convolutional layer, Pooling layer, and fully connected layers. 

![alt text](../Images_for_DBS101/CNN.png)

1. **Convolutional layer**: This layer is the first layer that is used to extract the various features from the input images. In this layer, We use a filter or Kernel method to extract features from the input image.
![alt text](../Images_for_DBS101/convolutional.png)

2. **Poooling layer**: The primary aim of this layer is to decrease the size of the convolved feature map to reduce computational costs. This is performed by decreasing the connections between layers and independently operating on each feature map. Depending upon the method used, there are several types of pooling operations. We have Max pooling and average pooling.

    ![alt text](../Images_for_DBS101/pooling.png)

3. **Fully-connected layer**: The Fully Connected (FC) layer consists of the weights and biases along with the neurons and is used to connect the neurons between two different layers. These layers are usually placed before the output layer and form the last few layers of a CNN Architecture.

### Advantages of Convolutional Neural Networks (CNNs):
- Good at detecting patterns and features in images, videos, and audio signals.
- Robust to translation, rotation, and scaling invariance.
- End-to-end training, no need for manual feature extraction.
- Can handle large amounts of data and achieve high accuracy.

### Disadvantages of Convolutional Neural Networks (CNNs):
- Computationally expensive to train and require a lot of memory.
- Can be prone to overfitting if not enough data or proper regularization is used.
- Requires large amounts of labeled data.
- Interpretability is limited, it’s hard to understand what the network has learned.

## Obeject Detection

Object detection is a computer vision technique that allows us to identify and locate objects in an image or video. With this kind of identification and localization, object detection can be used to count objects in a scene and determine and track their precise locations, all while accurately labeling them.

Imagine, for example, an image that contains two cats and a person. Object detection allows us to at once classify the types of things found while also locating instances of them within the image.

![alt text](<../Images_for DAM101/cats_and_person.jpg>)

### How object detection works

- **Input Data**: The system starts with an image or video frame.

- **Feature Extraction**: Convolutional Neural Networks (CNNs) extract important features like edges.

- **Region Proposal**: Methods like Selective Search or Region Proposal Networks (RPN) suggest potential object locations.

- **Classification and Localization**: Models such as Faster R-CNN, YOLO, or SSD classify objects and refine bounding box coordinates around detected objects.

    - **Faster R-CNN**: Proposes regions first, then classifies objects and refines boxes.

    - **YOLO**: Divides the image into a grid and predicts boxes and classes in one pass.

    - **SSD**: Uses multiple feature maps at different scales for detection in a single step.

- **Post-Processing**: Non-Maximum Suppression (NMS) removes redundant boxes, keeping only the most confident detections.

- **Output**: The result is a set of bounding boxes with class labels and confidence scores for each detected object.


### Use cases and applications

**Self-driving cars**

Real-time car detection models are key to the success of autonomous vehicle systems. These systems need to be able to identify, locate, and track objects around them in order to move through the world safely and efficiently.

![alt text](<../Images_for DAM101/self-driving.png>)

**Video surveillance**

Because state-of-the-art object detection techniques can accurately identify and track multiple instances of a given object in a scene, these techniques naturally lend themselves to automating video surveillance systems.

![alt text](<../Images_for DAM101/survillance.png>)

<p style="text-align: center;">THANK YOU:)</p>


