# heart2
Inspiration
Heart disease is a leading cause of death worldwide, and early detection can save lives. However, datasets related to heart attacks are often imbalanced, with fewer cases of heart attack incidences compared to non-heart attack cases. This imbalance can negatively impact machine learning models, making them biased toward the majority class. Inspired by the power of Generative Adversarial Networks (GANs), we aimed to generate synthetic heart attack data to balance the dataset and improve prediction accuracy.Due to high pollution the rate of heart attacks has also increased significantly

What it does
Our project uses a GAN to generate synthetic data that mimics real heart attack cases. This synthetic data is then combined with real data to create a more balanced dataset. We train a Random Forest classifier on this augmented dataset, improving the model’s ability to predict heart attack incidences more accurately.

How we built it
Data Preprocessing – We selected key numerical features related to heart attack risks, including BMI, cholesterol levels, alcohol consumption, and air pollution index. These features were normalized using MinMax scaling.

GAN Implementation – We designed a GAN consisting of:

A generator, which creates synthetic heart attack cases using random noise.

A discriminator, which learns to distinguish between real and synthetic cases.

The GAN training process, where both models compete to improve data generation quality.

Synthetic Data Generation – Once the GAN was trained, we used it to generate synthetic heart attack cases to balance the dataset.

Model Training & Evaluation – A Random Forest classifier was trained using a combination of real and synthetic data, and its accuracy was evaluated.

Challenges we ran into
Class Imbalance – Training models on highly imbalanced data led to biased predictions. Generating synthetic data helped address this issue.

GAN Training Stability – We encountered challenges such as mode collapse, where the generator produced repetitive outputs instead of diverse synthetic samples. Fine-tuning hyperparameters helped stabilize training.

Data Quality Validation – Ensuring that the synthetic samples improved classification performance without introducing noise required extensive testing.

Accomplishments that we're proud of
Successfully trained a GAN to generate synthetic heart attack cases.

Balanced the dataset, leading to improved classification accuracy.

Developed an effective machine learning pipeline integrating deep learning and traditional classification methods.

First heart attack model predictor taking air pollution into account

Achieving accuracy 91.9%

What we learned
The effectiveness of GANs in handling class imbalance in medical datasets.

The importance of tuning GAN parameters for stable training.

The impact of synthetic data augmentation on improving machine learning models.

What's next for Heart Attack Prediction using GAN
Enhancing the GAN Model – Exploring advanced GAN architectures such as Wasserstein GANs (WGANs) or Conditional GANs (cGANs) for more realistic data generation.

Feature Expansion – Including additional health indicators like blood pressure, genetic history, and physical activity levels for better predictions.

Clinical Validation – Collaborating with medical professionals to verify the model’s effectiveness in real-world scenarios.

Deployment – Developing an interactive tool that hospitals and doctors can use for early heart attack risk assessment.
