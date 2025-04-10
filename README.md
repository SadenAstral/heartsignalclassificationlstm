# Heart Signal Classification of R-R segmented ECG data using LSTM

Using R-R segmented ECG signals to classify cardiovascular abnormalities related to ventricular depolarizations, to five classes of ssociation for the Advancement of Medical Instrumentation (AAMI) standard.
(ref:https://pmc.ncbi.nlm.nih.gov/articles/PMC4897569/)

## Dataset:
Preprocessed R-R ECG signals from the MIT-BIH Arrhythmia Database https://www.physionet.org/content/mitdb/1.0.0/ taken from https://www.kaggle.com/datasets/shayanfazeli/heartbeat
Comprising-
Normal Beats(0): 72,471 samples
Ventricular Ectopic Beats-VEB(4): 6,431 samples
Supraventricular Ectopic Beats-SVEB(2): 5,788 samples
Fusion Beats - F(1): 2,223 samples
Unknown/Unclassifiable Beats(3): 641 samples

## Results:
98.6% accuracy on the testing dataset.

| Class Label | Description                          | F1 Score |
|-------------|--------------------------------------|----------|
| I.          | Normal (0)                           | 0.9913   |
| II.         | Fusion Beats (1)                     | 0.7877   |
| III.        | Supraventricular Ectopic Beats (2)   | 0.9460   |
| IV.         | Unclassifiable Beats (3)             | 0.8077   |
| V.          | Ventricular Ectopic Beats (4)        | 0.9856   |

### Confusion Matrix

| True\Pred |    0    |   1   |   2   |   3   |   4   |
|-----------|---------|-------|-------|-------|-------|
| **0**     | 18030   | 31    | 39    | 8     | 10    |
| **1**     | 140     | 384   | 32    | 0     | 0     |
| **2**     | 43      | 3     | 1384  | 16    | 2     |
| **3**     | 19      | 0     | 17    | 126   | 0     |
| **4**     | 27      | 1     | 6     | 0     | 1574  |


