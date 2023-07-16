# Improved Prediction for Failure Time of Multilayer Ceramic Capacitors
[![DOI](https://zenodo.org/badge/625665396.svg)](https://zenodo.org/badge/latestdoi/625665396)

This study introduces a novel machine learning model (MLM) developed using the eXtreme Gradient Boosting (XGBoost) method. The model is designed to predict the mean time to failure (MTTF) of multilayer ceramic capacitors (MLCCs) under various temperature and voltage conditions. Our approach aims to overcome the limitations of conventional models and provide a more accurate prediction of MLCCs' lifetime.

## Methodology

Our methodology involves two primary steps:

1. **Initial Utilization of HALT:** We determine the MTTF of X7R MLCCs under isothermal conditions at various temperatures and DC fields. A MLCC is declared as failed when the leakage current exceeds 300 µA. This initial step allows us to understand the basic failure conditions of the MLCCs and provides a foundation for the development of our machine learning model.

2. **Development of the MLM:** We employ the eXtreme Gradient Boosting (XGBoost) method to develop a physics-based machine learning model (MLM). The model is designed to predict the lifetime of MLCCs accurately. The model is developed with two primary objectives:

    a) Improving prediction accuracy for test conditions with limited data.
   
    b) Providing predictions for test conditions where no experimental data exists.

The model is fine-tuned on the available experimental data and then further fine-tuned on an EM-generated dataset using shared voltage conditions. This approach allows the model to address the limitation of TPM's accuracy caused by limited availability of data.

We present the flowchart for our machine learning approach in Figure 1.

![Figure 1: Flowchart for our machine learning approach.](resources/flowchart.png)

## Equations

The equations for TPM and EM are as follows:

TPM:

$$ln(t) = C(T) - ln[sinh(\frac{\beta E_{app}}{T})]$$


EM:

$$\frac{t_1}{t_2} = (\frac{V_2}{V_1})^n.exp[\frac{E_a}{k_B}(\frac{1}{t_1}-\frac{1}{t_2})]$$

where t, V, T, n, $$k_B$$, $$E_a$$ are the lifetime of MLCCs, applied voltage, temperature, the electric-field acceleration factor, Boltzmann’s constant, and activation energy of mobility governing the degradation process, respectively.

These equations represent the conventional models for predicting MTTF, which our MLM aims to improve upon.

## Results and Discussion

Our MLM outperforms conventional models in predicting the MTTF of X7R MLCCs. We show the results in Figure 2, which displays the RMSE and RMSPE scores for each model. 

![Figure 2: RMSE and RMSPE scores for each model.](figure2.png)

We argue that our MLM can deliver superior performance and stability compared to conventional models. We also note that predicting the entire distribution for lifetime of MLCCs is necessary to achieve a valid reliability estimate. We suggest that predicting the variance of the distribution could be a complementary factor for thorough reliability analysis. 

## Future Work

The next phase of the ongoing work would be to predict the variance of the distribution as a complementary factor for thorough reliability analysis. This would provide a more comprehensive estimate of the lifetime distribution, further improving the reliability estimate.

## Acknowledgements

This work is supported by the National Science Foundation, as part of the Center for Dielectrics and Piezoelectrics (CDP) under Grant Nos. IIP-1841453 and IIP-1841466.

## Conflict of Interest

The authors declare no conflict of interest.

## Data Availability

The data and source code that support the findings of this study are available at the Zenodo repository (https://doi.org/10.5281/zenodo.7943453) and source code developed openly at the GitHub repository (https://github.com/asepehri93/MLCC-LifeTime-Prediction).

## References

Various references are cited throughout the paper.
