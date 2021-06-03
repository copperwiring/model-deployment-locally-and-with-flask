In this tutorial we take the image classification model built in `model.py` which recognises Google Street View House Numbers. Using Flask to create an API, we can deploy this model and create a simple web page to load and classify new images. 

To run locally:

- Install pip and Python 3
- Clone this repository `git clone https://github.com/elliebirbeck/model-deployment-flask.git`
- Navigate to the working directory `cd model-deployment-flask`
- Install the Python dependencies `pip install -r requirements.txt`
- The project expects an additonal data ` extra_32x32.mat` (not present here due to the size) in the working directory. You can download the data from here: http://ufldl.stanford.edu/housenumbers/ 
- Get model pickel using `python model.py`.
- Run the API `python api.py`
- Open a web browser and go to `http://localhost:8000`

![screenshot.png](screenshot.png)

**Note:** Though it is recommended that you run `model.py` to generate your own pickled model, picked model used for testing can be found [here](https://drive.google.com/file/d/1HeKrKr7NqiYjz5zCTcgEfMO6-EZtAiut/view?usp=sharing). This was created using `scikit-learn==0.21.3` and can be tested with this. `scikit-learn` doesn't support pickling and unpickling across different version [[Source](https://github.com/scikit-learn/scikit-learn/issues/16570)].