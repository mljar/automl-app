
# New way for building ML pipelines!

We are working on new way for Python visual programming.  We developed desktop application called [MLJAR Studio](https://mljar.com). 
It is a notebook based development environment with interactive code recipes and managed Python environment. All running locally on your machine. We are waiting for your feedback.

It has [code recipes](https://mljar.com/docs/python-automl/) to build ML pipelines with MLJAR AutoML.

<p align="center">
  <img 
    alt="mljar AutoML"
    src="https://raw.githubusercontent.com/pplonski/pplonski/main/media/piece-of-code.png" width="77%" />  
</p>

---

# AutoML Web App 🤖

<p align="left">
<a href="https://github.com/mljar/mljar-supervised">🚀 AutoML</a>
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
 <a href="https://github.com/mljar/mercury">📓 Mercury</a>
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
<a href="https://github.com/mljar/automl-app/issues">🤝 Issues</a>
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
<a href="https://twitter.com/MLJAROfficial">🐦 Twitter</a>
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
<a href="https://www.linkedin.com/in/aleksandra-p%C5%82o%C5%84ska-42047432/">👩‍💼 LinkedIn</a>
 <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
<a href="https://mljar.com">🌐 MLJAR Website</a>
</p>


This is a Web Application designed to train Machine Learning pipelines using MLJAR AutoML, specifically tailored for tabular data. All the generated models are compressed into an archive format, allowing their reuse to compute predictions in batch mode.

This repo consists of three notebooks:
- [notebook](https://github.com/mljar/automl-app/blob/main/train-automl.ipynb) for training AutoML with simple UI,
- [advanced notebook](https://github.com/mljar/automl-app/blob/main/train-automl-advanced.ipynb) for training AutoML with more advanced UI (you can select feature engineering methods, algorithms, validation strategy, and evaluation metric),
- [notebook](https://github.com/mljar/automl-app/blob/main/automl-predict.ipynb) for computing predictions.


The Web App harnesses the capabilities of [mljar-supervised](https://github.com/mljar/mercury) to construct the Machine Learning pipeline with AutoML. This involves the automation of several key tasks:
- data preprocessing,
- features engineering,
- algorithm selection & tuning,
- ML models explanations,
- automatic documentation.
<p>
<img src="https://github.com/mljar/automl-app/blob/main/media/pipeline_AutoML.png" width="100%" alt="Supervised learning"></img>
</p>

The Web App is created directly from Jupyter Notebooks with [Mercury](https://github.com/mljar/mercury) framework.

### Demo



https://github.com/mljar/automl-app/assets/6959032/3363631a-2187-44cd-94a8-3cbd5418de98



### Online demo

The Web App is available online at [automl.runmercury.com](https://automl.runmercury.com). Input data upload is limited to 1MB.

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-online.png" alt="AutoML Web App online"></img>
</kbd>

### Run locally 🖥️

Please run the below commands to run Web App locally. It requires Python >= 3.8.

```bash
pip install -r requirements.txt
mercury run
```
 
### Training Notebook 📓

If you would like to increase the input file limit, please change the cell:

```python
data_file = mr.File(label="Upload CSV with training data", max_file_size="1MB")
```

and set your `max_file_size`.

Please change the following cell to increase training time:

```python
time_limit = mr.Select(label="Time limit (seconds)", value="60", choices=["60", "120", "240", "300"])
```

Times are in seconds. Please just increase the values.

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/notebook.gif" alt="AutoML training notebook"></img>
</kbd>

### Training models in Web App

Please upload a CSV file with training data, select input features & target, and click `Start training`.

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app.gif" alt="AutoML training in Web App"></img>
</kbd>

All models created during the training are available for download as a zip file:

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-download.gif" alt="AutoML models available for download"></img>
</kbd>

### Advanced Training Notebook 💪

Please use advanced mode if you would like to tweak AutoML parameters:

<kbd>
<img src="https://github.com/mljar/automl-app/blob/main/media/web-app-advanced.gif" alt="Advanced AutoML training notebook"></img>
</kbd>

## 👩‍💼🐦 Connect with Us on LinkedIn & Twitter

Stay up-to-date with the latest updates about MLJAR 🎨🤖 by following us on Twitter ([MLJAR Twitter](https://twitter.com/MLJAROfficial)) and LinkedIn ([Aleksandra LinkedIn](https://www.linkedin.com/in/aleksandra-p%C5%82o%C5%84ska-42047432/) & [Piotr LinkedIn](https://www.linkedin.com/in/piotr-plonski-mljar/)). We look forward to connecting with you and hearing your thoughts, ideas, and experiences.


### Good luck with ML training!
