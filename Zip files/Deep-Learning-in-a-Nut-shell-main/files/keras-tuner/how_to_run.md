# Hyper Parameter tuning using Keras-tuner


### Install the project
- Clone the repo
- Create a virtualenv and activate it:
```
conda create keras_tuner python=3.7
conda activate keras_tuner
```
- Install the requirements:
```
pip install requirements.txt
```


### Results

Tasks duration was measured on an RTX 2080 GPU

| Tuner                 | Search time   | Best accuracy (%) |
|-----------------------|---------------|-------------------|
| Worst Baseline       | 20min | 63.1             |
| Default Baseline      | 20min | 74.5              |
| Random Search         | 10h 59min  | 76.8              |
| Hyperband             | 10h 0min   | 75.1              |

Here, the worst baseline is the worst accuracy obtained by a set of hyperparameters 
during random search.
The default baseline is obtained by setting all hyperparameters to their default value.

### Run the baseline

```
python baseline.py
```

### Run the comparison
Available tuners :

- Random Search
- Hyperband

```
python tuner_comparison.py
```
