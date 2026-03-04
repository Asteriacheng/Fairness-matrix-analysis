# Fairness-matrix-analysis
This project explores credit risk prediction and fairness evaluation in data-driven lending systems. Access to credit plays a critical role in shaping life opportunities, yet modern credit scoring models raise important ethical and governance concerns when predictive performance interacts with potential structural or demographic disparities.

The analysis is based on a 5,000-row random sample** from the Home Credit Default Risk dataset, partitioned into a training set (4,000 observations) and a held-out test set (1,000 observations). The outcome variable is binary default risk (TARGET), with a naturally imbalanced default rate reflecting real-world credit scoring environments.

Two logistic regression models are constructed. The baseline model focuses on core financial and stability indicators such as income, age, household structure, and employment proxies. The extended model incorporates contextual and demographic features as well as external risk scores (EXT_SOURCE variables). While the extended model achieves improved ranking performance (AUC ≈ 0.766 compared to 0.655), decision-level evaluation shows that high predictive accuracy does not necessarily translate into meaningful risk discrimination, as the chosen threshold produces extremely low true positive detection.

Model evaluation combines predictive performance and ethical auditing. ROC curves and AUC are used to measure ranking quality under class imbalance, while fairness diagnostics are conducted across gender, age groups, and regional categories. Metrics include approval rate disparities, error rate gaps related to equal opportunity and equalised odds, and calibration assessment.

The project emphasizes that fairness cannot be reduced to a single statistical metric. Threshold selection, probability calibration, data provenance, and downstream decision use are treated as integral components of responsible model design. In particular, external scoring features may act as opaque information channels, potentially embedding upstream biases into prediction pipelines.

Overall, this study demonstrates the tension between predictive optimisation and ethical deployment in credit scoring systems, highlighting the importance of transparency, governance, and socio-technical evaluation in algorithmic decision-making.
