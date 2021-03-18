# Development of a system for modeling the dependence of electricity consumption and economic indicators
Digital breakthrough hackathon final (2020) - data science part of the project

6th place out of 25 projects in the final

---

## Demo
![](https://i.imgur.com/icFzkG7.png)

## Results
Developed **model for prediciton of energy consumption** using different metrics.

Description of models:
- Model A --- simple one-series multilayer perceptron
- Model B --- multi-series multilayer perceptron

Using metrics:
- Power supply reliability assessment
- The rate of increasing of living and business areas
- Manufacturing volume

Description of the table:
- Input window --- size of input time series for predicitons
- Output window --- size of output time series
- Compression --- size of input time series from raw dataset that we replace by mean value
- Epochs --- number of training epochs
- Error --- relative error 
- Validation plot --- plot with blue part of real values and orange part of predicted values
- Future plot --- plot with prediciton of future energy consumption

| Model | Compression | Input window | Output window | Epochs | Error | Validation plot                      |
|-------|-------------|--------------|---------------|--------|-------|--------------------------------------|
| A     | 24          | 1 year       | 1 year        | 2000   | 5.0%  | ![](https://i.imgur.com/YimTlC4.png) |
| B     | 24          | 1 year       | 1 year        | 2000   | 5.0%  | ![](https://i.imgur.com/lZaKqr7.png) |
| A     | 24          | 2 years      | 2 years       | 2000   | 5.7%  | ![](https://i.imgur.com/ygMDTVT.png) |
| B     | 24          | 2 years      | 2 years       | 2000   | 4.9%  | ![](https://i.imgur.com/OowkFXo.png) |
| A     | 24          | 3 years      | 3 years       | 2000   | 4.8%  | ![](https://i.imgur.com/7PPG4fM.png) |
| B     | 24          | 3 years      | 3 years       | 2000   | 5.1%  | ![](https://i.imgur.com/yrLG5fX.png) |


## Usage 
### Requirements 
- python3 and pip3
```
sudo apt install python3
sudo apt install python3-pip
```

- jupyter notebook
```
pip3 install notebook
```

- tensorflow and other requirements from file
```
pip3 install tensorflow
pip3 install -r tensorflow requirements.txt
```

### Work with Jupyter Notebook
- Run cell with import

![](https://i.imgur.com/6DIwIXs.png)
- Set training parameters
![](https://i.imgur.com/Kgc1bLs.png)
- Next cell will parse dataset from national electicity database
- Load&prepare datasets
![](https://i.imgur.com/N5I4FbX.png)
- Next cell train simple one-dimensional model without additional metrics
![](https://i.imgur.com/Qnx0MlI.png)
- Generate plot with real values (blue part) and fitted values (orange part). Generate plot with predictions for future. You can see RMSE also.
![](https://i.imgur.com/hhlP5tS.png)
- Train multidimensional model
![](https://i.imgur.com/hhlP5tS.png)
- Generate validation plot, predictions plot for electicity consumption and our metrics.
![](https://i.imgur.com/FNOcoZH.png)

