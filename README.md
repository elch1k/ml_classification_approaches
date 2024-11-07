# Pet project of mushroom classification by using Machine Learning algorithms

Not really too complicated pet project for the implementation of data preparation and preprocessing and then subsequent classification modeling by using ML algorithms. Data source for this project was UC Irvine Machine Learning Repository with [mushroom dataset](https://archive.ics.uci.edu/dataset/848/secondary+mushroom+dataset).

The main goal of the project was short EDA and modeling which you can find in notebook by this [link](https://github.com/elch1k/mushroom_classification/blob/main/mushrooms_classification.ipynb) with full report.

Here I wanna share my results of modeling and share some of my thoughts about it. So, results of modeling you can see in table below:
| Model                       | Accuracy | Precision | Average Precision | F-score  | ROC-AUC  | Training Time (s) |
|-----------------------------|----------|-----------|-------------------|----------|----------|-------------------|
| Random Forest               | 0.998415 | 0.998521  | 0.997514          | 0.998310 | 0.998397 | 5.185778          |
| XGBoost                     | 0.997821 | 0.997676  | 0.996448          | 0.997676 | 0.997812 | 1.037126          |
| KNN                         | 0.995345 | 0.995769  | 0.992764          | 0.995032 | 0.995283 | 0.018723          |
| LightGBM                    | 0.995345 | 0.995559  | 0.992667          | 0.995033 | 0.995296 | 0.662788          |
| Decision Tree               | 0.993265 | 0.992194  | 0.988767          | 0.992822 | 0.993276 | 0.464818          |
| GradientBoostingClassifier  | 0.924128 | 0.932244  | 0.887710          | 0.917846 | 0.922943 | 9.675702          |
| SVC                         | 0.866779 | 0.881902  | 0.810277          | 0.853342 | 0.864424 | 131.939399        |
| ADA Boost                   | 0.784073 | 0.761252  | 0.698693          | 0.773436 | 0.784187 | 2.212214          |
| Logistic Regression         | 0.735737 | 0.709448  | 0.646694          | 0.723981 | 0.735935 | 1.917551          |
| Gaussian                    | 0.642135 | 0.586138  | 0.563354          | 0.678587 | 0.651712 | 0.060200          |

By logic of the data we should as possible as we can predict poisonous mushrooms, so for that the best metric to evaluate model accuracy is precision. From that we can see that Random Forest is the best model for this by precision, but if we a looking for the fastest and a relative accurate model, we can use KNN, what truly unexpectable for me. But after that prediction, we should get average metrics by cross validation of Random Forest, which I pick for that to objectively evaluate the model. And after cross validation we get prety good metrics like: *average F-score: 0.998, average of average precision score: 0.9999, average ROC-AUC: 0.9999 and average Cross-Entropy: 0.014896* and from this we we still get really impressive metrics, what means that previous modeling wasn't just lucky random seed.
**In conclusion, write again that the best model by performance is Random Forest.**
