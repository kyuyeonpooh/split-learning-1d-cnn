## Can We Use Split Learning on 1D CNN for Privacy Preserving Training?

**Note:** this repo contains our implementation for our ACM ASIACCS 2020 paper below. Please if you find it useful, use the below citation to cite our paper.

Sharif Abuadbba, Kyuyeon Kim, Minki Kim, Chandra Thapa, Seyit A. Camtepe, Yansong Gao, Hyoungshick Kim, Surya Nepal, ‘Can We Use Split Learning on 1D CNN Models for Privacy Preserving Training?’, The 15th ACM ASIA Conference on Computer and Communications Security (ACM ASIACCS 2020), Taipei, Taiwan, from June 1st to June 5th, 2020


**Available Now:**
- Our 1D CNN split learning models with their accuracy results.
- Our pre-processed training/testing samples of MIT arrhythmia ECG database.
- Our privacy leakage 3 measurements results using visual invertibility; distance correlation; and Dynamic Time Warping.
- Our proposed two countermeasures results: i) increasing the number of layers in a CNN model and ii) using differential privacy.

**Repository summary**
- `csv` directory: results in `csv` format from various kinds of experiments.
  - `adding_layers` directory: experiment results of **adding more convolutional layer** on 1D CNN.
    - `accuracy` directory: has best test accuracy data retrieved from each run with different number of convolutional layers.
    - `trainlog` directory: has train loss, train accuracy, test loss, test accuracy data for each epoch while training 1D CNN having different number of convolutional layers.
  - `diffpriv` directory: experiment results of **applying differential privacy on split layer** in 1D CNN.
    - `accuracy` directory: has best test accuracy data retrieved from applying different strength of differential privacy.
    - `trainlog` directory: has train loss, train accuracy, test loss, test accuracy data for each epoch while training 1D CNN whose split layer is differential private.
  - `measurement` directory: 
    - `dcor` directory: has distribution and mean of **distance correlation** data from each split layer filter.
    - `dtw` directory: has distribution and mean of **DTW** data from each split layer filter.
  - `split_nonsplit` directory: has train log data from split and non-split 1D CNN which are used to prove that they have same results.
- `figure` directory: source codes in `ipynb` format which give figure with data in `csv` directory.
- `measurement` directory: source codes in `ipynb` format which **measure distance correlation and DTW** between raw data and data from split layer filters.
  - `adding_layers` directory: measure distance correlation with different number of convolutional layers.
  - `diffpriv` directory: measure DTW with different strength of differential privacy on split layer.
- `mitdb` directory: has **preprocessed train and test data** in `hdf5` format.


