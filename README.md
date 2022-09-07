# Moving-target-sound-and-seismic-signal-dataset

This dataset contains four files, which are array files in python's .npy format.
Included “train_v_x.npy”, “train_s_x.npy”, “train_y.npy”, “validation_v_x.npy”, “validation_s_x.npy”, “validation_y.npy”.

train_v_x.npy is the training dataset of the seismic signal, which is a two-dimensional array of 6809 segments of 40,000 sampling points. The size of this array is (6809, 40000). 
train_s_x.npy is the training dataset of the sound signal, which is a two-dimensional array of 6809 segments of 40000 sampling points. The size of this array is (6809, 40,000). 
train_y.npy is the 6809 labels of the training dataset, where 0 is the noise signal, 1 is the pedestrian movement signal, and 2 is the vehicle movement signal. The labels correspond to the signals in order, for example, the first number in the train_y.npy is the label for the first sound and the first seismic signal.
validation_v_x.npy is the testing dataset of the seismic signal, which is a two-dimensional array of 1226 segments of 40000 sampling points. The size of this array is (1226, 40000). 
validation_s_x.npy is the testing dataset of the sound signal, which is a two-dimensional array of 1226 segments of 40000 sampling points. The size of this array is (1226, 40,000). 
validation_y.npy is the 1226 labels of the training dataset, where 0 is the noise signal, 1 is the pedestrian movement signal, and 2 is the vehicle movement signal. The labels also correspond to the signals in order, for example, the first number in the train_y.npy is the label for the first sound and the first seismic signal.

A sample read procedure is：

import numpy as np
label = np.load('train_y.npy')
