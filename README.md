# Make It Count  —  A Fashion Recommender

<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>


***Julia Zimpel***

***Full-Time Data Analytics 2020-08, Campus Berlin, 09 Oct. 2020***

**Repository: <Link> (https://github.com/Yulizzz123/final_project)**  
   
   
## Content    
        
    
**1. Project Description**

In today's fast-moving world of **quick real-life encounters**, fashion becomes the more crucial in presenting oneself, and leaving a lasting impression on other people. The situation has been hightened by Covid-19 where leaving the home has become severely restricted, and dressing up is a rare chance to 'make it count'. 

At the same time, general interest in **street-fashion** over Haute Couture rises. At the end of 2019, Amazon released the app 'StyleSnap' which allows people to take pictures of favored fashion pieces, and receive purchase recommendations in the online shop. 

This project seeks to develop a model that recommends fashion for **women** after having classified an input image according to clothing type and color. The following rules are applied:

| Input Image | Recommended  |
|:------------| :----------- |
| Top         | Skirt        |
| Skirt       | Top          |
| Dress       | Dress        |

Since many women do not wish to be suspected of wearing the same clothes on two subsequent days (unpublished survey), a fashion piece of a **different color** is recommended. 
    
Recommenders may benefit several parties. Companies may increase **revenue and customer satisfaction** through cross-selling, while customers may **save time** in purchasing multiple items at once as well as in finding **favored choices**. Hence, this project is also a contribution to  the study of **business-customer interactions**.         

  
**2. Methodology**

This project is mainly written in Python. For image recognition the state-of-the-art method of **Convolutional Neural Networks (CNN)** is employed by using the Tensorflow. CNN is a method from Deep Learning which has a higher efficiency and accuracy than other image recognition methods, such as kNN. For color detection, **kNN** is sufficient, and hence employed.
    
Two workbook series (A and B) are created with a sample size of **12,000 (A)** and **1,500 (B)** images. While series A achieves a **higher model accuracy** in image recognition, series B allows for **higher flexibility** in adjusting statements and parameters due to its smaller requirement on processing capacity. Hence, B was created before moving to the larger sample of A.
    
Working with large data volumes has led to the application of following insights for faster processing:
    
| No. | Principles                                                                                             |
|:----|:-------------------------------------------------------------------------------------------------------|
| 1.  | Images are shrunk in size for deep learning.                                                           |
| 2.  | Rather than creating long functions, code is split up into small components, and batches are employed. |
| 3.  | To avoid long reruns of code, modules and separate worksheets are created.                             |  

    
**3. Questions and Hypotheses** 

The model is created with **6 convolutional and pool layers and pools** to which the input sequentially passes.
    
Adjusting the hyperparameters, the following has proven to achieve an optimal result with the data at hand:

| No. | Findings                                                                         |
|:----|:---------------------------------------------------------------------------------|
| 1.  | 6 convolutional and pool layers rather than smaller and higher numbers of layers |
| 2.  | 96 filters rather than a mix of 32, 64 and 96 filters                            |
| 3.  | 512 neurons rather than 128 neurons                                              |
| 4.  | Adding a dropout layer                                                           |
| 5.  | A dropout layer of 70% rather than 50% or 90%                                    |
| 6.  | 15 epochs rather than 10, 12 or 20                                               |

The large sample size of series A with 12,000 images achieves a test accuracy of **72%**, while the smaller sample size of series B with 1,500 images achieves a test accuracy of **65%**. The difference of only **7 percentage points lower** of test accuracy of an **eight times** smaller sample size suggests that by choosing the right hyperparamters already considerable results can be obtained.  

    
**4. Dataset**

The following sample datasets are used in the project:

| Category | Number of Images | A Selected Images | B Selected Images |
|:---------|:-----------------|:------------------|:------------------|
| Tops     | 10,078           | 4,000             | 500               |
| Skirt    | 12,742           | 4,000             | 500               |
| Dress    | 60,768           | 4.000             | 500               |

Since the samples are considerable low, only **10% of A and B respectively** are for testing to reserve a maximum amount of images for training.     
    
    
**5. Database**

The DeepFashion database contains over **800,000** images. From this the attribute prediction subset of **290,000** images is selected, of which further **subsets** for training and testing are formed (see dataset). 

"DeepFashion" <Link>(http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion.html)
"Attribute Prediction" <Link>(http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion/AttributePrediction.html)

For testing with a different database, the Fashion Product Image database is used, which comprises 44,440 images.
"Fashion Product Images" <Link>(https://www.kaggle.com/paramaggarwal/fashion-product-images-dataset)  

    
**6. Workflow**
    
| No. | Activity                               |
|:----| :--------------------------------------|
| 1.  | Clean Data                             |
| 2.  | Develop Models for Image Recognition   | 
| 3.  | Test Models  for Image Recognition     |
| 4.  | Develop Model for Color Recognition    |
| 5.  | Issue Recommendation                   |  

    
**7. Organization**

The project folder contains the following files:

| No. | File                          |
|:----|-------------------------------|
| 1.  | README                        |
| 2.  | A1_Data_Preprocessing         |
| 3.  | A2_Extract_Transform          |
| 4.  | A3_Create_and_Test_Model      |
| 5.  | A4_Recommendation             |
| 6.  | B1_Data_Preprocessing         |
| 7.  | B2_Extract_Transform          |
| 8.  | B3_Create_and_Test_Model      |
| 9.  | B4_Recommendation             |
| 10. | AB_Data_Wrangling_New_Test    |  

    
**8. Next Steps**
    
Next I will increase the test accuracy of my model by adjusting further hyperparameters and the model's architecture.
Moreover, I will incorporate a recommendation engine based on deep learning in this project.   
    
       
**9. Sources**
    
The following sources have been used in this project:
    
Image Recognition in Python with TensorFlow and Keras <Link> (https://stackabuse.com/image-recognition-in-python-with-tensorflow-and-keras/)
    
Flower Classification with Deep Neural Network with Tensorflow and Python Programming <Link> (https://www.youtube.com/watch?v=POO1gdUJ7yE)
    
Classify Images Using Convolutional Neural Networks <Link> (https://medium.com/@randerson112358/classify-images-using-convolutional-neural-networks-python-a89cecc8c679)

Deep Transfer Learning for Image Classification <Link> (https://towardsdatascience.com/deep-transfer-learning-for-image-classification-f3c7e0ec1a14)


