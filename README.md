Mushroom Classification
This project trains a machine learning model to classify mushrooms as poisonous or edible based on their characteristics.

Usage
The Jupyter notebook mushroom_classification.ipynb trains a random forest classifier on the mushroom dataset. It contains the following steps:

Load and explore the mushroom dataset
Preprocess data (encoding categorical variables, handling missing values)
Split data into training and validation sets
Train a random forest classifier
Evaluate model on validation set
Fine-tune hyperparameters
Visualize feature importances
The trained model is saved to rf_model.pkl which can be loaded for prediction.

python


Copy code
import pickle
model = pickle.load(open('rf_model.pkl', 'rb'))
Pass input features to the model's predict method to predict if a mushroom is poisonous (0) or edible (1).

Data
The mushroom dataset is loaded from the UCI Machine Learning Repository. It contains 8124 instances with the following attributes:

cap-shape: bell, conical, etc.
cap-surface: scaly, grooves, etc.
cap-color: brown, yellow, etc.
bruises: bruises, no bruises
odor: almond, fishy, etc.
gill-attachment: attached, free, etc.
gill-spacing: close, crowded, etc.
gill-size: broad, narrow
gill-color: black, brown, etc.
stalk-shape: enlarging, tapering
stalk-root: club, equal, etc.
stalk-surface-above-ring: fibrous, scaly, etc.
stalk-surface-below-ring: fibrous, scaly, etc.
stalk-color-above-ring: brown, white, etc.
stalk-color-below-ring: brown, white, etc.
veil-type: partial, universal
veil-color: brown, white, etc.
ring-number: none, one, two
ring-type: cobwebby, evanescent, etc.
spore-print-color: black, brown, etc.
population: abundant, clustered, etc.
habitat: grasses, leaves, etc.
The target variable is class with two values - edible or poisonous.

Model
A random forest classifier is trained with 100 trees. The hyperparameters are tuned using randomized search cross-validation. The model achieves over 99% accuracy on the validation set.

The feature importances plot shows that the most important features are odor, gill-attachment, gill-spacing, and stalk-surface-below-ring.

References
The mushroom dataset is originally from the Audobon Society Field Guide to North American Mushrooms (1981).

UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/Mushroom

Let me know if you need any clarification or have additional suggestions to improve this README!
