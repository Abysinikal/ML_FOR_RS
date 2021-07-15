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



## References 
- Helber, P., Bischke, B., Dengel, A. and Borth, D., 2018. Eurosat: A novel dataset and deep learning benchmark for land use and land cover classification. arXiv preprint arXiv:1709.00029.
