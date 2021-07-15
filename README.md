# Machine Learning for Remote sensing : Random Forest vs Neural Networks
 
In this project,we are building two classifiers determining the land use and land cover classification of Sentinel-2 satellite images (EuroSAT dataset). The first model uses the Random Forest algorithm while the second uses the ResNet50 CNN algorithm. 
The project is therefore a comparative analysis of the two models trained on the same EuroSAT dataset. The EuroSAT dataset can be downloaded from http://madm.dfki.de/downloads. For more information please refer to [Helber et al. (2018)](https://arxiv.org/abs/1709.00029)




## Models 
### Pre-Processing
There is an important preprocessing step where :
-training and testing directories and respective subdirectories are created 
-StratifiedShuffleSplit from sklearn.model_selection module is used to random 
80% to 20% train/test split while moving the images to subdirectories
-We created ImageDataGnerator Instance for data augmentation

### Training


In the first model, We implement a simple RandomForestClassifier. The training time is 11 roughly minutes. 

In the second model, we implement CNN ResNet-50 model. The trainig time is multiple hours. (Refer to attached python notebooks for details as i commented and also left all outputs after each run).
Importrant to note that I custom run the training to run 2 epochs only for time saving purposes but ideally N_EPOCHS=50. 

## Evaluation
You will find here the evaluation of the two models 

![CMX_RF](https://user-images.githubusercontent.com/62526508/125800173-b5418904-974d-48d8-8b53-1c2b00f8d49b.png)
![CMX_CNN](https://user-images.githubusercontent.com/62526508/125800164-92650f79-4323-4df8-b2e4-db7a4b3ec1bd.png)
![CLR_RF](https://user-images.githubusercontent.com/62526508/125800179-bdf2daa9-bc6a-4969-81f2-29ef31bea854.png)
![CLR_CNN](https://user-images.githubusercontent.com/62526508/125800205-8ccbd681-e50e-4aea-8672-f982ca587a14.png)


## References 
- Helber, P., Bischke, B., Dengel, A. and Borth, D., 2018. Eurosat: A novel dataset and deep learning benchmark for land use and land cover classification. arXiv preprint arXiv:1709.00029.
