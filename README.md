# TOSEM2021Data

Data for ACM Transactions on Software Engineering and Methodology 2021 paper: `An Empirical Study of the Impact of Hyperparameter Tuning and Model Optimization on the Performance Properties of Deep Neural Networks`

There are two folders in this package: `SubjectData` and `Results`.

### SubjectData folder

- `Data` contains the details of different DNN model hyperparameter combinations come from hyperparameter tunning and the measured performance metrics come from inferencing standard DNN models and optimized DNN models of four representative and widely-used DNN models, namely `CNN image classification`, `Resnet-50`, `CNN text classification`, and `LSTM sentiment classification`.

  - To understand the impact of hyperparameter tuning on the performance of the DNN models and optimized DNN models, we structure our experiments along with some commonly-used hyperparameters in practice into three dimensions, including `D1: architecture-related hyperparameters`, `D2: layer-level model training decisions`, and `D3: optimizer hyperparameters`. The detailed description and search space of each hyperparameter used in our subject DNN models are shown in Table 2 of our paper.

  - Our DNN models are deployed and inference on multiple platforms, including `Server` and `Mobile devices`, thus, for investigating the effects of tuning different hyperparameters on DNN models and the optimized models for mobile devices, we focus on the evaluation of the DNN models on different representative perspectives, including `inference accuracy`, ` inference latency`, `model size`, ` number of floating-point operations`, and `battery consumption`. 
  - In particular, due to the characteristics of  different platforms, we evaluate **standard DNN models** with `inference accuracy`, ` inference latency`, `model size`, and `number of floating-point operations`; we evaluate **optimized DNN models** with `inference accuracy`, ` inference latency`, `unencoded model size`, `encoded model size`, `number of floating-point operations`, and `battery consumption`. 

- `Scripts` includes the python scripts for tuning  hyperparameters and optimizing standard DNN models for our subject DNN models.

  In particular, to successfully run these scripts (tunning hyperparameter and optimization) on your servers, you need to have at least `TensorFlow (version 2.2.0)`, `Keras Tuner`, and `TensorFlow Model Optimization Toolkit` installed. For more detailed information about the hardware and environment for `Server` and `Mobile devices` used in this study, please check Section 3.4 of our paper.

### Results folder

- This folder contains the spreadsheet files and box plots (in PDF format) that shows the results used to answer our two research questions: 

  - `RQ1`: What is the impact of tuning different hyperparameters on the performance of DNN models?
  - `RQ2`: What is the combined impact of hyperparameter tuning and model optimization on the performance of optimized DNN models?

  These results are based on our analysis of different hyperparameter selections and measured performance properties from our  subject DNN models, i.e., `CNN image classification`, `Resnet-50`, `CNN text classification`, and `LSTM sentiment classification` on two different platforms, including `Server` and `Mobile devices`.

