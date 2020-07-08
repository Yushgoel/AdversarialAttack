# AdversarialAttack
Creating an Adversarial Attack and Implementing Techniques to prevent them.

In this repository, I have created a jupyter notebook that tries out different techniques to make Deep Neural Networks more robust to Advesrarial Attacks.

Summary of Results

Model | Standard Accuracy | Adversarial Accuracy | Generalizes Noise(>30% on more noise) | Generalize Attack
----- | ----------------- | -------------------- | ------------------------------------- | -----------------
Standard CNN | 0.98 | 0.23 | No | -
Trained On Adver | 0.98 | 0.61 | No | -
Denoising (constant) | 0.98 | 0.91 | No | -
Remove Advers (Model) | 0.97 | 0.83 | Yes | No
Batch Norm (test time) | 0.97 | 0.69 | Yes | -
Dropout (test time) | 0.96 | 0.79 | Yes | Yes
Denoising (Autoencoder) | 0.95 | 0.84 | Yes | Yes
Dropout + Batch (test time) | 0.97 | 0.69 | - | -
Hypothesis Testing | Invalid | Invalid | Invalid | Invalid




Conclusion:

If Application permits 2 models - Use Denoising AutoEncoder + Standard Model
If only 1 model is feasable - Use Dropout (find values using gridsearch)
