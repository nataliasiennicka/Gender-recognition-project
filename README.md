# Gender-recognition-project

The project was made on the basis of data from the kaggle portal. The dataset contains a set of 202,599 tagged photos. Below are some sample photos from the dataset.

![image](https://user-images.githubusercontent.com/94246903/181916953-d944c929-ee1f-47f2-a751-a9fb56f99262.png)

In addition to the face photo files, a file with information about the gender of each person in the photo based on the photo name was attached.With this information, the model can be taught to recognize the gender of the person in the photo.

In the file containing descriptive data, a column called "Male" was found, which determines whether the person in the photo is male or female (1- male, 0 - female).
There are no missing values in the data, so there is no need to edit or delete items. Additionally, the balance of the data set was checked and the result was: 58% of women and 42% of men, which means a good balance of the set.

## Data splitting
To divide the data, the patrition file included in the output data was used, which contains the information to divide the set into training, validation and test data. The number of photos in each subset is as follows:
- training: 162 770
- validation: 19962
- test: 19867

Generators for grouping images (ImageDataGenerator) were used to create subsets. For this purpose, folders and subfolders were created in the work environment, in which the photos in the diagram were placed:
 - train:
      - female
      - male
 - valid
      - female
      - male
 - test
      - female
      - male
      
 ## Modele
 The project used models of neural networks in which the parameters were changed. Below is a comparison of the parameters used and the results for the models.
 
![image](https://user-images.githubusercontent.com/94246903/181918507-b2c06be8-d871-4995-b00c-f39a67f9eb75.png)
![image](https://user-images.githubusercontent.com/94246903/181918610-2e0d3859-c8f2-4c23-8286-7ae27ae78bea.png)
![image](https://user-images.githubusercontent.com/94246903/181918869-09c15611-236d-45bb-9f83-5de5b70fd8e5.png)

## Checking the predictions of the best model on an example
Since the model 3 gives the best results, it was checked what effects it gives on photos outside the set.

![image](https://user-images.githubusercontent.com/94246903/181919026-2cbb7d4f-84bd-4b9d-ac6e-b73f9f265ef9.png)
Image from: https://in.pinterest.com/pin/free-image-on-pixabay-beauty-woman-face-portrait-hair--578571883387085626/

Success! The model shows that there is a woman in the photo.
