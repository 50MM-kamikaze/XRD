# INTRODUCTION
This report explores the application of machine learning techniques to automate the
classification of peaks in XRD patterns, enabling efficient and accurate material
characterisation. The process involves data preparation, feature extraction, clustering for
auto-labelling, model training, and the classification of new XRD patterns. By leveraging
machine learning algorithms, engineers can streamline material analysis, enhance quality
control, and advance research in civil engineering.
X-ray powder diffraction (XRD) is a rapid analytical technique primarily used for phase
identification of a crystalline material and can provide information on unit cell dimensions.
The analysed material is finely ground, homogenised, and average bulk composition is
determined.

# DATASET DESCRIPTION
To embark on this study, a diverse collection of XRD patterns from civil engineering
materials was compiled. The patterns, stored as CSV files, include the "Angle" (scattering
angle) and "Intensity" (diffraction intensity) columns. These files were organized in the
"XRD_csv" folder for easy access and systematic analysis.
## Auto Labeling:
1. To streamline the peak classification process, the dataset underwent auto-labeling.
A clustering algorithm, specifically KMeans clustering, was employed to group XRD patterns
with similar characteristics into clusters. The number of clusters was set to three, representing
three distinct peak types that may correspond to different materials or phases. The cluster
labels were used as auto-generated ground truth labels for model training.
## New XRD Pattern:
1. As a real-world demonstration, a new XRD pattern named "OPCM-14D 2.csv" was
introduced into the dataset. The features of this pattern were extracted using the same
methodology as the other patterns. The trained classifier then predicted the type of peaks in
this new pattern, providing valuable insights into its material composition and structure

## DATASET DETAILS
Number of XRD Patterns: The dataset comprises a collection of XRD patterns from a diverse
range of civil engineering materials. It includes concrete, cement, clay minerals, soil samples,
and other construction materials.
1. File Format: Each XRD pattern is stored as a CSV (Comma-Separated Values) file.
Each file contains two columns: "Angle" and "Intensity." The "Angle" column represents the
scattering angle of the diffracted X-rays, while the "Intensity" column corresponds to the
intensity of the diffraction peaks at different angles.
2. File Organization: All CSV files are organized in a folder named "XRD_csv" to
ensure easy access and systematic analysis.

# Algorithm Description:
The algorithm employed in this study aims to automate the peak classification in X-ray
diffraction (XRD) patterns obtained from various construction materials used in civil
engineering. The goal is to accurately identify different peak types in the XRD patterns,
corresponding to different materials or phases, using machine learning techniques.
  1. Data Preparation:
The XRD patterns, collected from diverse sources, are stored as CSV files in the "XRD_csv"
folder. Each file contains two columns: "Angle" and "Intensity." The "Angle" column
represents the scattering angle of the diffracted X-rays, and the "Intensity" column contains
the intensity of the diffraction peaks at different angles.
  2. Feature Extraction:
Prior to model training, relevant features are extracted from each XRD pattern. In this study,
the feature extraction technique calculates two statistical measures: the mean and standard
deviation of the "Intensity" values. These features provide a concise representation of the
unique characteristics of each pattern, making them suitable for machine learning analysis.
  3. Clustering for Auto Labeling:
To facilitate automated labeling, a clustering algorithm, specifically KMeans clustering, is
utilized. KMeans is a partition-based clustering method that groups patterns with similar
characteristics into clusters. In this study, the number of clusters is set to three, representing
three distinct peak types that might correspond to different materials or phases.
  4. Model Training:
The Random Forest classifier is chosen for its ability to handle non-linear relationships and
multiple features effectively. The classifier is trained using the features extracted from the
XRD patterns and the labels obtained from the clustering step. The model learns to map the
extracted features to the auto-generated ground truth labels, enabling peak classification.
  5. Model Evaluation:
To assess the model's performance, the dataset is split into a training set and a validation set.
The training set is used to train the Random Forest classifier, while the validation set is used
to evaluate the model's accuracy, precision, recall, and F1 score. This rigorous evaluation
ensures the reliability and generalization of the trained model.
  6. Classification of New XRD Patterns:
To demonstrate the algorithm's practical application, a new XRD pattern named "OPCM-14D
2.csv" is introduced. The features of this pattern are extracted using the same methodology as
the other patterns. The trained Random Forest classifier then predicts the type of peaks in this
new pattern, providing valuable insights into its material composition and structure.

- To make the code work , change the names of the files and folders accordingly 
