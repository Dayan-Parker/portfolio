# Projects

- **Speech Speech Recognition Neural Net**:

In this project, I trained RNN and CNN models to classify both spoken digits (0–10) and the speaker's gender, achieving close to 100% accuracy with low false negative and false positive rates. The RNN model directly processed speech waveforms to leverage the sequential nature of the data, while the CNN was trained on spectrogram representations of the waveforms.

A significant challenge was the highly imbalanced dataset, with 90% male and 10% female samples, which severely impacted the models' ability to accurately classify the speaker's gender. Initially, I attempted to balance the dataset by removing excess male samples, but this approach left insufficient data for effective training. To address this, I implemented SMOTE (Synthetic Minority Oversampling Technique), a method I discovered in an academic blog. Using SMOTE, I generated artificial female samples by taking each existing female sample’s k nearest neighbors, randomly selecting one and then taking the convex combination of those two samples, significantly improving the dataset's balance and increase the size of the data set.

The CNN architecture, which classified spectrograms, was inspired by VGG16. It featured an increasing number of convolutional filters at each layer, with max pooling and batch normalization applied after every layer to enhance feature extraction and network stability. The RNN architecture included 1-D convolutional layers before the recurrent sections, abstracting features to enable higher-level pattern recognition. These convolutional layers were followed by two LSTM layers that utilized gated units to mitigate the vanishing and exploding gradient issues common in RNNs.
For training both networks, I employed the Adam optimizer, which combines momentum and adaptive learning rate techniques. This approach accelerated convergence and reduced the likelihood of getting stuck in local minima.


<img src="Dayan Parker_Mini Project Presentation-1.png" alt="Dayan Parker Mini Project Presentation](https://github.com/Dayan-Parker/portfolio/blob/main/Dayan%20Parker_Mini%20Project%20Presentation-1.png)" style="width:100%; height:auto;">


<div style="text-align: center;">
    <a href="https://dayan-parker.github.io/portfolio/project.html">Home</a>
</div>





