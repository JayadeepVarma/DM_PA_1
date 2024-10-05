# DM_PA_1
# README for Programming Assignment 1

## Questions and Outputs

### 1. Cropping and Resize Images in Your 4-class Images Dataset
**Question:**
Use the bounding box information in the Annotations dataset relevant to your 4-class Images Dataset to crop the images in your dataset and then resize each image to a 128×128 pixel image.

**Output:**
Classes in Image Directory:  
['n02092002-Scottish_deerhound', 'n02093428-American_Staffordshire_terrier', 'n02094114-Norfolk_terrier', 'n02110958-pug']  
The total Images in four classes are: 768  
Classes in Annotation Directory:  
['n02092002-Scottish_deerhound', 'n02093428-American_Staffordshire_terrier', 'n02094114-Norfolk_terrier', 'n02110958-pug']  
The total Annotations in four classes are: 768  
Images are cropped.

---

### 2. Feature Extraction: Edge Histogram and Similarity Measurements
**Question:**
Choose 1 image from each class, convert them to grayscale, and compute edge histograms. Then, perform histogram comparison between two edge histograms using Euclidean, Manhattan, and Cosine distances.

**Output:**

![image](https://github.com/user-attachments/assets/1061edd5-7cb1-42d6-bbec-9a6a657234b2)
Angle:
[[2.91479381 0.9817665 1.40657798 ... 0.81029943 0.99935555
0.62463921]
[0.09065989 1.00955245 1.44916894 ... 0.53872997 0.52632182
0.24348783]
[0.78539816 1.07311647 1.46387339 ... 0.60547226 0.44252027
0.17016359]
...
[2.11121583 1.88328789 0.78539816 ... 2.36336208 3.10108732
0.21115697]
[0.11379201 2.39726727 1.99928255 ... 2.25770579 0.05127328

Histogram Data
(array([346, 369, 389, 391, 435, 390, 421, 448, 434, 433, 516, 494,
565,
593, 591, 650, 655, 672, 686, 640, 585, 555, 455, 459, 370,
398,
374, 358, 349, 299, 353, 333, 354, 357, 341, 326],
dtype=int64), array([0.04363323, 0.13089969, 0.21816616, 0.30543262,
0.39269908,
0.47996554, 0.56723201, 0.65449847, 0.74176493, 0.82903139,
0.91629786, 1.00356432, 1.09083078, 1.17809725, 1.26536371,
1.35263017, 1.43989663, 1.5271631 , 1.61442956, 1.70169602,
1.78896248, 1.87622895, 1.96349541, 2.05076187, 2.13802833,
2.2252948 , 2.31256126, 2.39982772, 2.48709418, 2.57436065,
2.66162711, 2.74889357, 2.83616003, 2.9234265 , 3.01069296,
3.09795942]))
![image](https://github.com/user-attachments/assets/a830ba1c-e5d3-4261-bfda-9d5148b53b67)
![image](https://github.com/user-attachments/assets/313a55d0-afc5-49e0-b0d1-9237f97d8152)
![image](https://github.com/user-attachments/assets/9fa54cdd-23ee-4298-8fc4-ed191b6c46e7)



The Distances for the edge histogram between datasets 1 and 3 are:  
Euclidean Distance: 827.82  
Manhattan Distance: 4062.0  
Cosine Distance: 0.0438

---

### 3. Histogram of Oriented Gradient (HOG) Feature Descriptor
**Question:**
Pick 1 image and compute its HOG descriptors. Visualize the image and the HOG descriptors.

**Output:**

![image](https://github.com/user-attachments/assets/e50b97df-4c96-4aaa-96e9-abf08157e171)

HOG Descriptors: [0.0, 0.0, 0.0, ..., 0.1283, 0.2731, 0.0952]

---

### 4. Dimensionality Reduction (using PCA)
**Question:**
Use images from all four classes, convert them to edge histograms, and perform PCA dimensionality reduction.

**Output:**
Histogram Data:  
[[-0.0379, 0.0033],  
[-0.0119, -0.0098],  
[0.0043, -0.0097],  
[0.0213, -0.0001],  
[-0.0044, 0.0092]]...

![image](https://github.com/user-attachments/assets/6445b9c1-ed87-4bab-b598-79c4f5b4e52b)

In the presented scatter plot it can be observed that there exist four classes which are
distinguished by four colors. Blue (Pug): There is some seperation but still overlaps with other
Red (American Staffordshire Terrier): Overlaps with other classes also Green (Norfolk Terrier):
Also overlaps Orange (Scottish Deerhound): In this case, there can be seen some divisions but
they still intersect. Based on this analysis there are no classes that are completely nonoverlapping.
However the blue class may contain some sites that appear visually different from
others but all cannot be said to be very different from other classes. Therefore existing classes
are not visually separable at all in this plot.

---

### 5. Text Processing Steps on a Tweet Dataset
**Question:**
What are the dimensionality of the two vector representations (token counts and TF-IDF)?

**Output:**

![image](https://github.com/user-attachments/assets/bdc724a6-f9c8-46ea-9ee2-3ec94f4b8da2)
![image](https://github.com/user-attachments/assets/98481eb4-a414-4122-bd50-741453993d1f)
First Plot: There is a huge amount of overlap between emotions in the plot which seems to
overlap which makes it difficult to distinguish any emotions are separable
Second Plot: Similar to the first plot there is also a overlap between emotions but there is a
slight separation for the joy emotion as they are isolated from the remaining points
In summary there might be a one visually separable class which can be joy which has minute
data points, but for the first plot there is no visually separable class.
