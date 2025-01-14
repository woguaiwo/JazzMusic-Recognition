# JazzMusic-Recognition

In 2024’ Fall semester, a student in our COMP major WeChat group asked for person who has done music recognition before. To be specific, he explained that he had around 80 Jazz music (3~5 min each) and would like to use some mature programs or algorithms help him to recognize the music according to some random 20s pieces. At that time, nobody answered him in the group, however, I naively think that such mission could be easily achieved by an overfitted neural network model. Additionally, I was concurrently self-learning Pytorch’s official RNN tutorials, so was excited about dealing with sequential data. As a result, I spent a whole week to develop a model for him. After some analysis, I consider RNN unrealistic to train the data, as a result, decided to apply CNN as the core structure. The initial version failed with only around 1.5% accuracy, as a result, I decided to halt and finish this project in winter. 

In winter vacation, I invited a friend to further develop the recognition model together. With huge uncertainty about how many parameters the model should possess, the data preprocessing methods, the sampling methods and the model structures, suitable hyper-parameters, we initially had no clues, and have done many trials.  

There were two major breakthroughs afterwards, the first one was that, we discovered the training feature (Mel-spectrogram) could be further compressed as the input of model. Additionally, with greater training epoch number, our model accuracy increased to around 45%. Then, we reflect upon this breakthrough, began focusing on understanding, and exploring music features. Eventually, we extracted 6 features, and used a similar way in RNN to combine them in a single CNN model, and reached an accuracy of around 96%.

Our further goals on this project, is to try out applying transformers to develop a music generator, plus, further improving original work to make the accuracy reaching 100%. 

