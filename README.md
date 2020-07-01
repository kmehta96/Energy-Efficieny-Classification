## PROJECT REPORT

## Data Set Description

The heating load (HL) and the cooling load (CL) is required for speciation of the cooling and
heating equipment when it comes to design efficient building, to maintain comfortable indoor air
conditions based on user requirements. To evaluate the required heating and cooling capacities in
the building, engineers and building designers need information about the characteristics of the
buildings and of the inured space (for instance orientation, occupancies and dimensions). For this
reason, the dataset consists of 8 input variables namely surface area, relative compactness, glazing
area distribution, overall height, orientation, wall area, glazing area and, roof area to determine the
output variables Heating Load and Cooling Load of residential buildings.

The dataset consists of 768 data points and 8 input features, aiming to classify two real valued
responses [1]. The labels are transformed into classes by approximating each class based on range
of data defined. The project looked into evaluating the cooling load and heating load requirements
of building as a function of building parameters to improve the efficiency of the building and
Energy analyzes using 12 different building shapes simulated in software Ecotect. The buildings
differ with respect to the orientation, the glazing area distribution, and glazing area, amongst other
parameters. The project converts to multi-class classification problem as it converts the responses
to rounded to the nearest integer and defining classes based on the range defined.

The dataset contains eight input features and two labels. The aim is to use the eight features to
predict each of the one response (Heating Load), Cooling Load is not considered as label in this
project.

Specifically:

- Relative Compactness
- Roof Area
- Surface Area
- Wall Area
- Glazing Area Distribution
- Orientation
- Glazing Area
- Overall Height
- Cooling Load
- Heating Load

In this project the aim is for classification, hence heating load is only considered for classification
by defining each class.


## Conclusion

The aim of this project is to classify Heating Loads in the building to determine the specifications
of the heating equipment needed to maintain comfortable indoor air conditions. The dataset
consists of 8 features while only heating load is considered as labels in this project with small data
points to train and test the model performance. Firstly, the heating load is available with floating
values and to convert into classification problem, the labels are divided into classes by defining
each class with range of values of the labels. The dataset is not uniformly distributed with the
number of classes defined and hence desired performance may vary.

In data cleaning, the statistics of the model is found and observed that the distribution of the dataset
does not consists of any missing values. While plotting the data in box plot, it was observed that
there were no outliers in the dataset. Hence the dataset does not require any cleaning methods to
perform. While plotting the correlation of the dataset it was observed that Orientation column is
not correlated with the any other feature. While the Glazing distribution and Glazing distribution
area are having very less correlation, which is also understood as if the area of the distribution is
high does not mean that the heating load required would be high. While the relative compactness
and the surface area are highly correlated but inversely. Based on the correlation matrix, the dataset
is greatly understood and by plotting in heatmap, the visualization of the correlation is greatly
enhanced.

Baseline model is developed with six models namely Logistic Regression, QDA, KNN, Decision
Tree, SVM and Random Forest. Initially all the models provide bad result as the validation set
approach is used and hence LOOCV cross validation technique are used to generalize the model
performance. Logistic Regression and QDA still does not perform well as the dataset are highly
non-linear and the decision boundary where linear and quadratic in nature for the respective
models. In feature reduction, two technique is used for model training namely by dropping
Orientation column from training the model as it consists of zero correlation among all other input
features. Another technique used for feature reduction is by using PCA with number of
components as six which means by dropping one feature and converting correlated data to
uncorrelated. With all the feature reduction technique all six models were trained and their
performance is noted. Lastly, PCA input features are used to train the model with LOOCV cross
validation technique which helps to further enhance the performance of the model.

In models with non-linear decision boundary, **Random Forest** performs best with **95% test
accuracy** by using PCA with LOOCV technique. As the model is generalized with the test data
by using cross validation technique and by using PCA correlation data converted to uncorrelated
as well as the number of features required to train the model has reduced. Hence the model is
neither overfitted nor under fitter and the best or the optimum performance model is obtained by
using Random Forest. To verify and understand the performance of the model, graphs are plotted
for precision and recall for each class as well as RoC curve is plotted by averaging the output of
each class and the area under the curve obtained is **0.79.**

In conclusion, with the help of machine learning the energy efficiency increase as we obtain some
inference regarding the type of input feature effected on the output and some correlation of the
input features. By using the model the heating load of the building will be obtained and will help


to improve the performance of the equipment by proper design the product. Similar to the heating
load, prediction or classification of the cooling load may be possible with the given dataset and
will be considered as the future scope of the project.
