# Movies-Recommender-System
In recent years, the explosion of data and the popularity of e-commerce and streaming platforms have made personalized recommendations a vital component of many businesses. From Amazon to Netflix, recommendation engines have become ubiquitous in modern online commerce. This repository provides access to the notebook used to obtain the results for a [technical report](https://drive.google.com/file/d/1fcvNiU6CGfjQSWAayQ-77xRBOr1Gk3GY/view?usp=sharing) showcasing a prototype of a recommendation engine we have developed and explaining its value to any business: a case study of Applied Machine Learning at Scale. 

Our recommendation engine is based on collaborative filtering, a technique that analyzes the preferences and behaviours of users to recommend items they might like. This is a popular technique for building recommendation systems, which relies on the idea that users with similar preferences will have similar preferences in the future. This method can be used for various item recommendations, such as books, music, and movies, and is effective in many real-world applications. Our prototype will use the Alternating Least Squares (ALS) algorithm, a matrix factorization method that can handle large datasets and effectively capture user-item interactions. Our engine also incorporates content-based filtering by considering movie genres to improve the accuracy of recommendations.

Our engine also incorporates content-based This is a simple unified framework for predicting stock prices using machine learning models from my [MSc Mathematical Sciences](https://drive.google.com/file/d/1PD7tn2eRz3VI0Xq71WBdmGFnBG7i5DLP/view?usp=sharing)  research project implemented in [TensorFlow](https://www.tensorflow.org). The project uses three deep neural network models: RNN, LSTM, and GRU to forecast stock time series data composed of closing prices of 8 indices of stocks listed on different stock markets. The selected indices are AEX index, DAXINDX, CAC40,
FTSE100, HNGKNGI, JAPDOWA, NASCOMP, and ATHEX Composite. Below is an illustration of how machine learning can be used in stock market prediction.

![alt text](https://drive.google.com/uc?id=1Pws9qssKrTc_PXQ7F_Q6NSPZjVJZDrVq) 

## RNN architectures
In this project, the following architectures for RNN, LSTM and GRU were used:
<div>
    <img src="https://drive.google.com/uc?id=1VbSAtIs5csGr6Sbj0a5mkyYzLnAJv2Y8" style="width: 46%; float: left;" />
    <img src="https://drive.google.com/uc?id=19HJkyy_Ki7zNj87PIliDnrMvjPsBlmar" style="width: 50%; float: right;" /> 
 </div>
 
## Experimental Results
Loss (MSE) committed by the three RNN variants during training and validation, and the results for AEX index prices predicted by the three RNN variants are shown below.
<div>
    <img src="https://drive.google.com/uc?id=1kNP2ZFQTzU-edRO3yXiLOCNB5JUIywtW" style="width: 46%; float: left;" />
    <img src="https://drive.google.com/uc?id=1aoQobTu0wJy_tWFBMpnFE-R8nZbb9klE" style="width: 50%; float: right;" /> 
 </div>

The figure below shows the actual stock prices of AEX index and the prices predicted by the three models with a rolling period of $P = 5$ and $10$ days respectively.

![alt text](https://drive.google.com/uc?id=1LJQ8xw1JC8VAW6ZdfnE5hgVspA8y2YTw)

After prediction was done on the test set, both the predicted and test target values were transformed back to real stock prices using the inverse linear transform function. The accuracy measures: MAE, RMSE, and MAPE are computed to evaluate the performance of each model. MAE, RMSE, and MAPE values for each of the three RNN models with a rolling period P = 5 and 10 days are shown in Tables 5.1a below.
![alt text](https://drive.google.com/uc?id=1FeQkxFoswFqAw50cyarFoSoSTWYw38Uh) 


## Running the code

### Dependencies
- TensorFlow
- Anaconda 3
- Python 3
- Any CPU/GPU-supported device

### Datasets
The historic stock prices dataset used in this project can be downloaded [here](https://drive.google.com/file/d/1R0IoeRv7bAw7rR4qsEDfn0rOyl7KpQp3/view?usp=sharing).

### License
Refer to the [LICENSE](https://github.com/naftalindeapo/Movies-Recommender-System/blob/main/LICENSE).
