# AutoML Web App

It is a Web App for training Machine Learning pipelines with MLJAR AutoML. It works with tabular data. All models are zipped to archive and can be reused to compute predictions in the batch mode.

This repo consists of three notebooks:
- [notebook](https://github.com/mljar/automl-app/blob/main/train-automl.ipynb) for training AutoML with simple UI,
- [advanced notebook](https://github.com/mljar/automl-app/blob/main/train-automl-advanced.ipynb) for training AutoML with more advanced UI (you can select feature engineering methods, algorithms, validation strategy and evaluation metric),
- [notebook](https://github.com/mljar/automl-app/blob/main/automl-predict.ipynb) for computing predictions.


### Demo

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/demo.gif" alt="AutoML Web App demo"></img>
</kbd>

### Online demo

The Web App is available online at [automl.runmercury.com](https://automl.runmercury.com).

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-online.png" alt="AutoML Web App online"></img>
</kbd>

### Run locally

Please run below commands to run Web App locally. It requires Python >= 3.8.

```bash
pip install -r requirements.txt
mercury run
```

### Training Notebook

If you would like to increast the input file limit please change the cell:

```python
data_file = mr.File(label="Upload CSV with training data", max_file_size="1MB")
```

and set your `max_file_size`.

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/notebook.gif" alt="AutoML training notebook"></img>
</kbd>

### Training models in Web App

Please upload CSV file with training data, select input features & target, and click `Start training`.

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app.gif" alt="AutoML training in Web App"></img>
</kbd>

All models created during the training are available for download as zip file:

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-download.gif" alt="AutoML models available for download"></img>
</kbd>

### Advanced Training Notebook

Please use advanced mode if you would like to tweak AutoML parameters:

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-advanced.gif" alt="Advanced AutoML training notebook"></img>
</kbd>
