# Appliance-EDA-Classification

(Go to https://github.com/DanielTranDS/Appliance-EDA-Classification/blob/main/AppliancesClassification_Codes.ipynb for implementation)
Greenhouse gas emissions have become an increasingly concerning issue across the globe. They result in climate change, which in turn have far-reaching environmental and health consequences. Energy production and consumption is the main contributor to greenhouse gas emissions. Furthermore, empirical study shows that electricity consumption in residential areas contributes to more than 20% of this total energy consumption.

In this project, I will be dealing with a time-series dataset. I will attempt to forecast the activation period for various appliances, all of which are commonly used in households in residential areas. This task can prove to be crucial because by using various machine learning techniques and correctly forecasting the activation period of appliances, we will have a better foresight of electricity consumption information, which in turn might provide valuable insights to come up with a better energy-saving technology.

There are 2 main challenges that we need to address, when it comes to the dataset given. The first challenge is how to effectively tackle a time-series dataset. The second challenge is, there are severe class imbalance issues for most of the target variables.

To tackle the first challenge, we employ a specific way of implementing cross validation, which we refer to as rolling fold cross validation. For the second challenge, we implement resampling to help alleviate the class imbalance issue. The resampling method that we used is undersampling, with additional modification to preserve the sequential structure of the data in a time-series dataset.

The aim is to develop multiple classifiers for each individual target appliance that can detect whether target appliances are being used in each time interval as correctly as possible. This means that I will develop 5 classifiers for 5 appliances.

train datafile contains 417720 instances, each of which has 15 columns, including load, 5 appliance labels (1 indicating using appliances and 0 indicating not using appliances), two time stamps (such as hour of the day and day of the week), and 7 attributes/features. The 5 appliances are air conditioner (ac), electric vehicle charger (ev), oven, cloth washer (wash), and dryer. Note that all the load data are minute-by-minute meter readings in a sequential manner.

test datafile contains 105540 instances, each of which has 10 columns, including load, two timestamps, and 7 attributes but no appliance labels.
