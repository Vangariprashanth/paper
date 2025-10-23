# 22 - Oct - 2025

1. put here yesterday's limitation
2. research about the publications
3. Read a paper and summarize
4. draft the paper

# Notes

https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10013431
https://norma.ncirl.ie/8615/1/aarthirajendran.pdf - This paper has UCF 101 dataset - which could be useful- https://www.crcv.ucf.edu/research/data-sets/ucf101/
8,000 labeled images,

- https://www.ejournal.isha.or.id/index.php/Mandiri/article/view/406/433 - This paper has CNN code
  current limitations - Angle based - Why the fail - **\*** Simple ML models and DL - Why simple ML models fail ? such as KNN, XGBoost, Randomforest fail - Work on feature engineering - normalization , random noises, removal of keypoints (occlusions) - There dataset is not robust - filming on various devices, outdoors, indoors, lightnings - All the papers consider single frame only - Include spatio-temporal thing - Mobile optimized - Lightweight CNN, Lightweight ViT - TinyML 1. Quantization aware training 2. Post training

justification of why our model works and why not others

https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9569773 - This paper has limitations of the ML models and why DL is used
" The first limitation in the existing literature on HIC is of
employing machine learning methods, such as Random Forest
and SVM that rely on domain-related features. However, some
studies [10] have been conducted to mitigate this problem
by incorporating the automatic feature extraction capability
of CNN. "

https://www.youtube.com/watch?v=P84OW5GovBE - CNN, RNN, LSTM

# 23 - Oct - 2025
Limitations discussed yesterday:
- Classical ML techniques
    - they depend on hand-constructed features instead of learning automatically
    - we will use hand-extracted (engineered) features, but the NN will learn features on its own
    - 3D CNN only works for a few frames - look into RNN, LSTM, Transformer
    - most papers only consider one frame at a time, we’ll use a time-based architecture
- we need datasets
    - our dataset
    - a standardized dataset
    - maybe one other dataset

Paper title: "Research on human movements push up counter based on media-pipe artificial intelligence"
Summary:
- uses mediapipe, data from 2 cameras at a front and side profile, and logic rules pertaining to good pushup form (angles, distances between body parts) in order to classify pushups.
- They use a Random Forest classifier to assess the accuracy of their method. It is unclear how that is done.

Limitations:
- Dataset is robust for a narrow task. 480,000 samples gathered from 50 videos. However, videos gathered only represent two angles - the front and side profiles. more videos including more angles would make the dataset more robust. I'm also unsure why they need a dataset, as the primary mode of classification seems to come from logic rules, not ML.
- Random Forest is used as a classifier. I don't know why people are still using classical ML instead of Neural Networks.
- Logic-based implementation. Assumes that Mediapipe will always return correct results. Not effective for noisy data, or cheating prevention.
- Uses data from two cameras to predict classes. Most users of an app like this will not have two cameras available. can we achieve the same results with one camera?

