# Project Rough Outline

1. key Libraries and Tools ⭐
   1. `tensorflow`, `keras` - Library
   2. `opencv` - Library
   3. `matplotlib` - Library
   4. **Google Colab**
2. Dataset Structure ⭐
   1. Top Level Folder
      1. Category-1
         1. Image-1
         2. Image-2
         3. .......
      2. Category-2
         1. Image-1
         2. Image-2
         3. .......
      3. .......
3. Loading Dataset into google drive
   1. So that you dont have to upload dataset everytime.
4. Model Compilation Training ⭐
   1. Trying Different Model Architectures
   2. And Comparing Model Performance
5. Saving the Model and Downloading into drive in Tensorflow
   1. So that once you trained the model it will saved and used later
6. Model Evaluation ⭐
   1. Accuracy
   2. Precision
   3. Recall
   4. f1-Score
   5. Confusion Matrix
7. Report ⭐
   1. Dataset description.
   2. Different Model Architectures that you trained.
   3. Model Evaluation Results.
   4. Challenges Faced.
8. Model Deployment (If Possible)
   1. In your Local Laptop

\
\
\
\
\
\
\
\

# Image Classification (CNN)

## 1. Fruit Classification Dataset ✅

1. **Dataset Link** - https://www.kaggle.com/datasets/icebearogo/fruit-classification-dataset
2. Contains 100 different classes of fruits for training Image classification model

This dataset contains 101 classes of different fruits. This dataset is perfectly suitable for someone trying to build image recognition models using deep learning or machine learning techniques. Each class has around 400 images for the training set, 50 for validation set and finally 50 for the test set.

#### Categories: (100)

1. abiu
2. acai
3. acerola
4. ackee
5. ambarella
6. apple
7. apricot
8. avocado
9.  banana
10. barbadine
11. barberry
12. . . . . . .  Total 100 Categories of Fruits

## 2. Mushroom species recognition ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/zlatan599/mushroom1

This dataset contains images of different mushroom species, divided into over 100 classes, each corresponding to a specific species. The images show mushrooms in various growth stages and conditions, making the dataset ideal for fine-grained classification tasks. The data is organized into three CSV files: train.csv for training, val.csv for validation and optimization of the model during training, and test.csv for the final performance evaluation. Each CSV file includes image paths and corresponding species labels, making it easy to use for machine learning models.

#### Categories : (100)

1. Agaricus augustus
2. Agaricus xanthodermus
3. Amanita amerirubescens
4. Amanita augusta
5. Amanita brunnescens
6. Amanita calyptroderma
7. Amanita citrina
8. Amanita flavoconia
9.  Amanita muscaria
10. Amanita pantherina
11. Amanita persicina
12. Amanita phalloides
13. Amanita rubescens
14. Amanita velosa
15. . . . Many More


## 3. Garbage Detection ❌

1. **Dataset Link** : https://www.kaggle.com/datasets/viswaprakash1990/garbage-detection

This dataset contains labeled images for garbage classification using object detection, formatted for use with YOLOv5 and similar models. It includes six classes of waste:

#### Categories: (6)
1. BIODEGRADABLE
2. CARDBOARD
3. GLASS
4. METAL
5. PAPER
6. PLASTIC

## 4. Cat Breeds Detection ✅

1. **Dataset Link** : https://www.kaggle.com/datasets/nikolasgegenava/cat-breeds

🚀 Ready to dive into the classification of cute cats? This dataset unveils a captivating collection of over 11,000 high-quality images spanning more than 60 distinct cat breeds. From the Bengal to the sleek Siamese, the fluffy Maine Coon to the curious Sphynx, you'll discover a stunning visual encyclopedia of our purr-fect companions 😁.

#### Categories : (60+)

1. abyssinian
2. american_bobtail
3. american_curl
4. american_shorthair
5. american_wirehair
6. balinese
7. bengal
8. birman
9.  bombay
10. british_shorthair
11. burmese



## 5. Popular Sneakers Classification ✅

1. **Dataset Link** : https://www.kaggle.com/datasets/nikolasgegenava/sneakers-classification

Popular and Modern Sneaker Image Classification dataset — a high-quality, clean collection of sneaker images built to help you train computer vision models!. Whether you're a fashion tech enthusiast, a machine learning enthusiast, or just passionate about streetwear and sneaker culture, this dataset offers everything you need to build robust models for sneaker classification.

#### Categories: (50)

1. adidas_forum_high
2. adidas_forum_low
3. adidas_gazelle
4. adidas_nmd_r1
5. adidas_samba
6. adidas_stan_smith
7. adidas_superstar
8. adidas_ultraboost
9.  asics_gel-lyte_iii
10. converse_chuck_70_high
11. . . . . .Many More



## 6. Musical Instruments ✅

1. **Dataset Link** : https://www.kaggle.com/datasets/nikolasgegenava/music-instruments

🎸 Musical Instruments Classification Dataset contains high-quality images of 10 iconic musical instruments from various genres and cultures. It is designed for image classification tasks in computer vision and can be used to train models to classify between visually distinct instruments. Each image is labeled with its corresponding instrument class, making the dataset ideal for educational tools, music-related applications, or AI-powered classifier systems.

#### Categories: (10)

1. accordion
2. banjo
3. drum
4. flute
5. guitar
6. harmonica
7. saxophone
8. sitar
9.  tabla
10. violin

## 7. Popular Street Foods Classification ✅

1. **Dataset Link** : https://www.kaggle.com/datasets/nikolasgegenava/popular-street-foods

This dataset is designed to support the development and evaluation of machine learning models for classifying images of popular street foods from around the world. It contains high-quality, labeled image data representing various street food categories commonly found in different regions and cultures.

#### Dataset: (20)

1. arepas
2. burger
3. bánh_mì
4. churros
5. crepes
6. currywurst
7. empanadas
8. falafel
9. fish_and_chips
10. gelato
11. hot_dog
12. kebab_(shish_kebab)
13. pad_thai
14. pani_puri
15. pizza_slice
16. poutine
17. pretzel
18. samosas
19. shawarma
20. tacos




## 8. Brain MRI Images for Brain Tumor Detection ✅

1. **Dataset Link** : https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection

#### Categories (2)

1. yes 
2. no


## 9. Satellite Image Classification ❌

1. **Dataset Link**: https://www.kaggle.com/datasets/mahmoudreda55/satellite-image-classification

The past years have witnessed great progress on remote sensing (RS) image interpretation and its wide applications. With RS images becoming more accessible than ever before, there is an increasing demand for the automatic interpretation of these images. In this context, the benchmark datasets serve as essential prerequisites for developing and testing intelligent interpretation algorithms. After reviewing existing benchmark datasets in the research community of RS image interpretation, this article discusses the problem of how to efficiently prepare a suitable benchmark dataset for RS image interpretation. Specifically, we first analyze the current challenges of developing intelligent algorithms for RS image interpretation with bibliometric investigations. We then present the general guidance on creating benchmark datasets in efficient manners. Following the presented guidance, we also provide an example on building RS image dataset, i.e., Million-AID, a new large-scale benchmark dataset containing a million instances for RS image scene classification. Several challenges and perspectives in RS image annotation are finally discussed to facilitate the research in benchmark dataset construction. We do hope this paper will provide the RS community an overall perspective on constructing large-scale and practical image datasets for further research, especially data-driven ones.

#### Categories: (4)

1. cloudy
2. desert
3. green_area
4. water

## 10. Chest X-ray Images ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/tolgadincer/labeled-chest-xray-images

This dataset contains 5,856 validated Chest X-Ray images. The images are split into a training set and a testing set of independent patients. Images are labeled as (disease:NORMAL/BACTERIA/VIRUS)-(randomized patient ID)-(image number of a patient). For details of the data collection and description, see the referenced paper below. According to the paper, the images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou.

#### Categories: (2)

1. NORMAL
2. PNEUMONIA

## 11. Mammals Image Classification Dataset (45 Animals) ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/asaniczka/mammals-image-classification-dataset-45-animals

The images are in the ImageNet structure, with each class having its own folder containing the respective images. The images have a resolution of 256x256 pixels. This original dataset contains images of 45 different classes of mammals.

#### Categores: (45)

1. african_elephant
2. alpaca
3. american_bison
4. anteater
5. arctic_fox
6. armadillo
7. baboon
8. badger
9. blue_whale



## 12. Cifar10 Classification Image ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/gazu468/cifar10-classification-image

The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.
The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than another. Between them, the training batches contain exactly 5000 images from each class.

1. airplane
2. automobile
3. bird
4. cat
5. deer
6. dog
7. frog
8. horse
9.  ship
10. truck

## 13. Animal Species Classification - V3 ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/utkarshsaxenadn/animal-image-classification-dataset

Animal Classification Dataset for Multi-Class Image Classification task. This is Animal Classification Data-set made for the Multi-Class Image Recognition Task. The dataset contains 15 Classes, these classes are :

1. Beetle
2. Butterfly
3. Cat
4. Cow
5. Dog
6. Elephant
7. Gorilla
8. Hippo
9.  Lizard
10. Monkey
11. Mouse
12. Panda
13. Spider
14. Tiger
15. Zebra


## 14. Apple Leaf Disease Symptoms Dataset ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/mhantor/apple-leaf-diseases

The Apple Leaf Diseases Dataset is a comprehensive collection of images that are instrumental in the study and identification of various foliar diseases in apple trees. This dataset is a valuable resource for researchers, data scientists, and machine learning enthusiasts who are interested in plant pathology and agricultural technology.

The purpose of this dataset is to aid in the development of machine learning models capable of identifying the categories of diseases (apple black rot, cedar rust, and scab leaf diseases) in apples, thereby contributing to more effective disease management strategies in apple cultivation.

1. Apple_black_rot
2. Apple_cedar_rust
3. Apple_scab


## 15. Sugarcane Leaf Disease Dataset ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/pritpal2873/sugarcane-leaf-disease-dataset

The health of the sugarcane plant can be inferred a great deal from these five sugarcane leaf states. Using this dataset, we can develop a computer vision system that can identify the condition of sugarcane plants based solely on their leaves and provide recommendations for managing those conditions.

The dataset has been captured with smart phones of various configuration to maintain the diversity. It contains total 2569 images including all categories. This database has been collected in Maharashtra, India. The database is balanced and contains good variety. The image sizes are not constant as it originates form various capturing devices. All images are in RGB format.


The Sugarcane Leaf Diseases Dataset is divided into five folders: a regular directory and four directories with photos of different types of sugarcane leaf diseases. The collection includes:

1. Healthy
2. Mosaic
3. Red Rot
4. Rust
5. Yellow

## 16. Maize Leaf - Disease Identification ✅

1. **Dataset Link**: https://www.kaggle.com/datasets/farmannaim/maizeleaf

Maize or corn (Zea mays L.) is an important cereal crop of the world. It is a source of nutrition as well as phytochemical compounds. Phytochemicals play an important role in preventing chronic diseases. It contains various major phytochemicals such as carotenoids, phenolic compounds, and phytosterols. It is believed to have potential anti-HIV activity due to the presence of Galanthus nivalis agglutinin (GNA) lectin or GNA-maize. A tablespoon of maize oil satisfies the requirements for essential fatty acids for a healthy child or adult. Decoction of maize silk, roots, leaves, and cob are used for bladder problems, nausea, vomiting, and stomach complaints. Zein an alcohol-soluble prolamine found in maize endosperm has unique novel applications in pharmaceutical and nutraceutical areas. Resistant starch (RS) from maize reduces the risk of cecal cancer, atherosclerosis, and obesity-related complications. This review presents a detailed view on the nutritional and potential health benefits of maize.


#### Categories :

1. Common Rust
2. Gray Leaf Spot
3. Healthy
4. Northern Leaf Blight
5. Not Maize Leaf

## MNIST in CSV (Hand written Digit Recognition)

1. **Dataset Link**: https://www.kaggle.com/datasets/oddrationale/mnist-in-csv

The mnist_train.csv file contains the 60,000 training examples and labels. The mnist_test.csv contains 10,000 test examples and labels. Each row consists of 785 values: the first value is the label (a number from 0 to 9) and the remaining 784 values are the pixel values (a number from 0 to 255).

#### Categories :

- Digit - 0
- Digit - 1
- Digit - 2
- Digit - 3
- Digit - 4
- Digit - 5
- Digit - 6
- Digit - 7
- Digit - 8
- Digit - 9
