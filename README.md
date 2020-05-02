# mlflow-sandbox

MLflow testing repository

## Table of Contents

- [mlflow-sandbox](#mlflow-sandbox)
  - [Table of Contents](#table-of-contents)
  - [Getting Started](#getting-started)
  - [Running a MLflow Example](#running-a-mlflow-example)
  - [History](#history)
    - [How mlflow env was created](#how-mlflow-env-was-created)
  - [Delete Conda Env](#delete-conda-env)
  - [MLflow Info](#mlflow-info)
    - [Entities](#entities)
    - [Modules](#modules)
      - [Tracking](#tracking)
      - [Models](#models)
      - [Projects](#projects)
    - [Big Tech Developments](#big-tech-developments)

## Getting Started

```bash
conda init
conda env create
conda activate mlflow
jupyter-notebook --no-browser
```

## Running a MLflow Example

Based on [MLflow Quickstart](https://www.mlflow.org/docs/latest/quickstart.html)

```bash
cd ~/repos && git clone https://github.com/mlflow/mlflow
cd ~/repos/mlflow/examples
mlflow ui
mlflow run sklearn_elasticnet_wine -P alpha=0.5
mlflow run sklearn_elasticnet_wine -P alpha=0.4
ls -l mlruns/0/
```

## History

### How mlflow env was created

```bash
conda init
conda create -n mlflow python=3.7.6 pip jupyter nb_conda ipykernel
conda activate mlflow
pip install mlflow
conda env export -f environment.yml
pip freeze > requirements.txt
```

## Delete Conda Env

```bash
conda deactivate
conda remove --name mlflow --all
```

## MLflow Info

Creado por Databricks, a su vez creado por Spark.

### Entities

Todo gira en torno a "Experiments" y "Runs".

### Modules

#### Tracking

Evolución del modelo.

#### Models

Deployment, conexiones a Azure por ejemplo.

#### Projects

Dejarlo en Git.

### Big Tech Developments

- FBLearner Flow (Facebook)
- TFX (Google)
- Michelangelo (Uber)
