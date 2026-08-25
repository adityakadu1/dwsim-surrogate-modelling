# dwsim-surrogate-modelling
tp create a surrogate on site model(decentralized) which provides dwsim(chem simulator) like answers for binary distillation cloumn without being computationally expensive , three models are implemented here and evalution matrics of each one is considered to decide the best possible model along with automatic data generation thorugh .net and pynet

## Prerequisites & Dependencies
* `pythonnet` (Provides the `clr` module to interface Python with DWSIM's .NET assemblies)
* `sys` (Standard library for system path references to DWSIM DLLs)
* `scikit-learn`
* `pandas`
* `numpy`
* `matplotlib`
* `joblib`

Install required packages via pip:
pip install pythonnet scikit-learn pandas numpy matplotlib joblib

##Software Requirements

* Windows OS (Required for .NET Framework / pythonnet)
* DWSIM v8.0+
* Python 3.9+
* Required packages: pip install numpy pandas scikit-learn matplotlib seaborn pythonnet joblib

## How to Run the Project

Run all python files in jupyter notebook or an equivalent ide

1.open folder names "code" to find all python scripts
Run file named "1_DataSampling" where you can also change the number of input samples created (4000 by me) by changing the 4000 in sampling(4000) in block 6 line 2. running whole code will save a csv file named "4kinput" 
this file is to be passed into file named "OutputAutomation" ( all done nothing extra work required)

2.the file named "MethodEval" do not help the surrogate in any way and is not part of model training process it is a mere dive and find approach done by me to find names and arguments different methods in DWSIM takes which are used by me further in the automation part, this file told me the nomenclature DWSIM use for different property which was very compulsory to know

3. the file named "OutputAutomation" is a ready to run file which takes in the "4kinput" csv file and give a csv file named "dwsim_surrogate_clean" this same file is provided under name Dataset.csv

4. all further three files names " 4_RandomForest", "5_SupportVecotrMachine", "6_ArtificialNeuralNetowrk" are model 
as the name of file suggests and use  the "dwsim_surrogate_clean" csv file for model training purpose and they print 
the Model evaluation metrics after training also each there are plots and graphs wherever felt required 

5. the file is just a block of code which provided a pictorial comparison between performance matrics of all outputs 
