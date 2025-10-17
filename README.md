# MATLAB Soil Bearing Capacity Predictor

An Artificial Neural Network (ANN) model built in MATLAB to predict the bearing capacity of spread footings in soil based on geotechnical parameters.

## 🚀 Project Overview
- **Problem:** Predicting soil bearing capacity is crucial for foundation design in civil engineering. However, accurate predictions of the bearing capacity require full-scale load tests that are usually very expensive, or model foundations plate load tests which are less expensive yet less accurate, or bearing capacity theories which the least expensive at the cost of accuracy.
- **Solution:** Developed a machine learning model using MATLAB's Neural Network Toolbox that takes soil parameters as input and outputs bearing capacity predictions, presenting itself as an optimal solution for the problem: a cheap yet accurate method of bearing capacity predictions.
- **Result:** Model achieved 96% accuracy/R² score on test data.

## 📁 Project Structure
```
soil-bearing-capacity-predictor/
├── BCDATA_EXPLORATORY_ANALYSIS &_PREPARATION.xlsx     # Data Preparation & EDA
├── BEARING_CAPACITY_DATA.xlsx                         # Entire Dataset - minimally processing
├── BearingCapacityNNetFxn.m                           # Function for saved trained model inference
├── BearingCapacityPredictingANN.mlapp                 # MATLAB App for model inference
├── BearingCapacity_ANNDevelopment.mat                 # Model development workflow
├── results/                                           # Generated plots and results
│   ├── error_comparative_analysis.png
│   ├── model_architchture.png
│   ├── model_matlab_app.png
│   ├── training_performance_error.png
│   └── training_performance_regression.png
└── README.md                                          # Readme file
```

## 🛠️ Technologies Used
- **Primary Platform:** MathWorks MATLAB R2022b
- **Toolboxes:** Neural Network Toolbox & feedforwardnet class

## 📊 Dataset Features
- Input parameters: Foundation width ($m$), Foundation length ($m$), Foundation embedment depth ($m$), Soil effective friction angle (degrees), Average effective unit weight ($kN/m^3$), Soil effective cohesion ($kN/m^2$), Soil effective stress ($kN/m^2$)
- Target variable: Bearing capacity ($kN/m^2$)
- Dataset size: 134 samples
- Data source: from literature

## 🧠 Model Architecture
- **Type:** Feedforward Neural Network
- **Layout:** [Input neurons (7)] - [Hidden layer neurons (10)] - [Output neuron]
- **Training Algorithm:** Levenberg-Marquardt optimization algorithm
- **Activation Functions:** Tan-sigmoid in hidden layers, Linear in output
- **Performance Function:** Mean Squared Error (MSE)

## 🚀 Installation & Usage

### Prerequisites
- MATLAB R2022b or newer
- Neural Network Toolbox and feedforwardnet class

### Running the Project
1. **Clone this repository**

2. **Open MATLAB and navigate to the project folder**

3. **Run the main model inference function**
   Run the ```BearingCapacityNNetFxn()``` function on the required data to infer the bearing capacity.

### Alternative to *step 3* (Recommended)
   - Run the matlab app ```BearingCapacityPredictingANN.mlapp```
   - enter required data
   - click on the **Execute** button to infer the bearing capacity

## 👨‍💻 Author
**Chrispin Emmanuel Phiri**
- Email: x6cemma@gmail.com
- LinkedIn: https://www.linkedin.com/in/chrispin-phiri-07880216a
- GitHub: https://github.com/XrisCP

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
