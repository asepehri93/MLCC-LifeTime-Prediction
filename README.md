# MLCC-LifeTime-Prediction
[![DOI](https://zenodo.org/badge/625665396.svg)](https://zenodo.org/badge/latestdoi/625665396)

# Improved Prediction for Failure Time of Multilayer Ceramic Capacitors

In this study, we present a physics-based machine learning approach to predict the mean time to failure (MTTF) of multilayer ceramic capacitors (MLCCs) under various temperature and voltage conditions. We contend that conventional models for predicting MTTF have limitations, and that our machine learning model can augment the accuracy of these models. 

We use a dataset of MLCCs with different target voltages and temperature conditions. We use the corresponding TPM parameters for each target voltage to create a dataset for pre-training. Once the base model is created, we fine-tune on the remaining experimental data, excluding the datapoint with the target voltage. We then evaluate our machine learning model (MLM) against the target voltage and compare its performance to that of TPM and EM. We use two evaluation metrics to compare the performance of the models: root mean square error (RMSE) and root mean square percentage error (RMSPE) scores.

Our MLM outperforms TPM and EM in predicting the MTTF of X7R MLCCs. We show the results in Figure 2, which displays the RMSE and RMSPE scores for each model. 

![Figure 2: RMSE and RMSPE scores for each model.](figure2.png)

We argue that our MLM can deliver superior performance and stability compared to conventional models. We also note that predicting the entire distribution for lifetime of MLCCs is necessary to achieve a valid reliability estimate. We suggest that predicting the variance of the distribution could be a complementary factor for thorough reliability analysis. 

We present the flowchart for our machine learning approach in Figure 1.

![Figure 1: Flowchart for our machine learning approach.](figure1.png)

The equations for TPM and EM are as follows:

TPM:

$$\frac{dN}{dt} = -\frac{N}{\tau}$$

where N is the number of failures, and τ is the time constant.

EM:

$$\frac{dN}{dt} = -\lambda N$$

where N is the number of failures, and λ is the failure rate.

In conclusion, we present a physics-based machine learning approach to predict the MTTF of MLCCs. We find that our MLM outperforms conventional models in predicting the MTTF of X7R MLCCs. We suggest that predicting the entire distribution for lifetime of MLCCs is necessary
