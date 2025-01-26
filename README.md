<h1 align="center">
  <img src="./logo.svg" height="300" width="300" alt="Logo Nome do Projeto" /><br>
  Applying Data Science Methodology to a Case Study: AI-Driven Medical Image Analysis
</h1>

![GitHub License](https://img.shields.io/github/license/antoniobiasotti/chest-vision?labelColor=101010)

Artificial Intelligence certainly can help doctors better understand high volumes of data, specially medical images, in a highly efficient way. By acting as a supportive diagnostic tool, it has the potencial to enhance precision and velocity in detecting diseases such as pneumonia. However, in many clinical cases, doctors still have to determina the exact reason why the model made each decision, so they can validate and trust the results. This need of trustworthiness is even greater in critical environments, such as hospitals, where diagnostic errors can have terrible consequences. With that being said, the problem question is: 

**Can we automatically identify pneumonia signals in medical X-ray images with high precision using machine learning techniques?**

## Stack

<!-- Linguagens -->
![Python](https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=FFD43B)

<!-- ML/AI -->
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)

## Execução

Antes de iniciar com o desenvolvimento e os comandos, é importante definir as variáveis de ambiente no seu ambiente de desenvolvimento. Abaixo a listagem de quais definir:

| Variável  | Tipo     | Necessidade            | Default | Descrição                  |
| :-------- | :------- | :--------------------- | :------ | :------------------------- |
| `EXAMPLE` | `string` | [Required \| Optional] | `Foo`   | Lorem ipsum dolor sit amet |

## Licença
This project is under [MIT - Massachusetts Institute of Technology](https://choosealicense.com/licenses/mit/). A short and simple permissive license with conditions only requiring preservation of copyright and license notices. Licensed works, modifications, and larger works may be distributed under different terms and without source code.

<hr>

## The Cross-Industry Standard Process for Data Mining Cycle (CRISP-DM)

![CRISP-DM Cycle](images/CRISP-DMCycle.png)

The first step in the Data Science Methodology is to determine the Analytic Approach by basically answering the question: How can data be used to solve the problem? In our case, since we will probably be dealing with raw images, an unstructured type of data, we need a technique that can handle complex visual patterns, such as Convolutional Neural Networks (CNNs), to extract meaningful features. On top of that, we are also doing a binary classification, where the model has to predict a yes/no value for the target variable based on other characteristics observed in each X-ray image of the patient lungs.  While CNNs are highly effective at capturing complex visual patterns in raw images, Random Forests offer more interpretability and can be used with extracted features from a pre-trained CNN. This dual approach will ensure a robust solution for pneumonia detection in X-ray images.

Moving on to the Data Requirements, in this stage we have to define the criteria of the data for the approach that was selected, as well as the data content, formats and sources. In our case, we require a large dataset containing binary-labeled (normal or pneumonia) chest X-ray images. It's an absolute must that the images are clear and of sufficient quality, so that the model will not have trouble with that. One other criteria is the volume, thousands of images are needed to deep learning models like CNN, and the data diversity, the dataset should include images from different sources, to guarantee the model can generalize well.

The next stage is Data Collection. The dataset will be collected from publicly available sources and integrated with the hospital's patients base. We will also must ensure the dataset is balanced, with a sufficient number of images for both 'pneumonia' and 'normal' classes. If needed, techniques like Data Augmentation are effective to increase size of the dataset and improve model generalization.

In the Data Understanding and Preparation stage we will explore the dataset to gain insights into its structure and quality. This includes visualization, EDA - Exploratory Data Analysis, to understand how both classes are distributed and address potential issues such as missing data or class imbalance. We also must care to what additional work is required to manipulate and work with the data, preparing for the next stage, where the model will in fact, learn how to classify. To prepare the data, we will preprocess the images by resizing them to a standard resolution (e.g. 224x224 pixels). Here in this stage we can also make use of data Augmentation techniques to and avoid overfitting, or we can come back here in later case we need. Using a pre-trained Convolutional Neural Network (CNN) we will extract high-level features from the images, these features will be flattened and, if necessary, reduced in dimensionality using PCA (Principal Component Analysis) to improve computational efficiency.  To close this stage, the dataset will be split into training, validation, and test sets.

Finally Modeling and Evaluation. It's here where the magic happens - we train and evaluate our model to classify X-ray images as 'pneumonia' or 'normal'!  Given the hybrid nature of our approach, we will first use a pre-trained Convolutional Neural Network (CNN) to extract high-level features from the images. These features will then serve as input to a Random Forest classifier, which will perform the final classification.   The performance of the Random Forest classifier is evaluated using the testing dataset. We calculate metrics such as accuracy, precision, recall, F1-score, and ROC-AUC to assess the model's effectiveness. 

Additionally, a confusion matrix displaying True Positives (TPR), False Negatives (FNR) False Positives (FPR) and True Negatives (TNR), is generated to visualize the model's predictions and identify any potential misclassifications. One last technique that can be applied is the LIME (Local Interpretable Model-agnostic Explanations) to interpret individual predictions. LIME highlights the regions of the X-ray images that most influenced the model's decision, providing transparency and increasing trust in the model's outputs.  

After Modeling and Evaluation, if the test were all succesful, we can just hope for the stakeholder's positive feedback! :)

Thx for reading.

### Author: Antônio Biasotti