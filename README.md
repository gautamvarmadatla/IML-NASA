## Predicting Solar Flares Using a Long Short-term Memory Network
[![DOI](https://github.com/ccsc-tools/zenodo_icons/blob/main/icons/lstm-flare-predict.svg)](https://zenodo.org/badge/latestdoi/433245747)

We present a long short-term memory (LSTM) network for predicting whether an active region (AR) would produce a ϒ-class flare within the next 24 hr. We consider three ϒ classes, namely ≥M5.0 class, ≥M class, and ≥C class, and build three LSTM models separately, each corresponding to a ϒ class. Each LSTM model is used to make predictions of its corresponding ϒ-class flares. The essence of our approach is to model data samples in an AR as time series and use LSTMs to capture temporal information of the data samples. Each data sample has 40 features including 25 magnetic parameters obtained from the Space-weather HMI Active Region Patches and related data products as well as 15 flare history parameters. We survey the flare events that occurred from 2010 May to 2018 May, using the Geostationary Operational Environmental Satellite X-ray flare catalogs provided by the National Centers for Environmental Information (NCEI), and select flares with identified ARs in the NCEI flare catalogs. These flare events are used to build the labels (positive versus negative) of the data samples. Experimental results show that (i) using only 14–22 most important features including both flare history and magnetic parameters can achieve better performance than using all 40 features together; (ii) our LSTM network outperforms related machine-learning methods in predicting the labels of the data samples. To our knowledge, this is the first time that LSTMs have been used for solar-flare prediction.

## Binder

This notebook is Binder enabled and can be run on [mybinder.org](https://mybinder.org/) by using the link below.


### run_FlarePredict.ipynb (Jupyter Notebook for FlarePredict)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ccsc-tools/LSTM-flare-prediction/HEAD?labpath=ccsc_FlarePredict.ipynb)

Please note that starting Binder might take some time to create and start the image.

For the latest updates of FlarePredict refer to [https://github.com/deepsuncode/LSTM-flare-prediction](https://github.com/deepsuncode/LSTM-flare-prediction)

## Installation on local machine

Note: Tested on Python 3.10.9

Installing below mentioned packages using conda:

```conda create -n <env-name> python=3.10.9 <library=version> <library=version> ...```

|Library | Version   | Description  |
|---|---|---|
|pandas|1.5.2|Data analysis and manipulation tool|
|scikit-learn| 1.2.0| Machine learning|
| tensorflow  | 2.10.0  | Neural network libraries  |
| keras  | 2.10.0   |Artificial neural networks API   |
|h5py| 3.7.0|Pythonic interface to the HDF5 binary data format|

## References

Predicting Solar Flares Using a Long Short-term Memory Network. Liu, H., Liu, C., Wang, J. T. L., Wang, H., ApJ., 877:121, 2019.

https://iopscience.iop.org/article/10.3847/1538-4357/ab1b3c

https://arxiv.org/abs/1905.07095

https://web.njit.edu/~wangj/LSTMpredict/
