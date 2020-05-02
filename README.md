# mlflow-sandbox

MLFlow testing repository

## Getting Started

```bash
conda init
conda env create
conda activate mlflow
jupyter-notebook --no-browser
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
