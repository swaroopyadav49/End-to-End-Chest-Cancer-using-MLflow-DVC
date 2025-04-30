# End-to-End-Chest-Cancer-using-MLflow-DVC

# Workflows

 1.Update config.yaml <br>
 2.Update secrets.yaml [Optional] <br>
 3.Update params.yaml <br>
 4.Update the entity <br>
 5.Update the configuration manager in src config <br>
 6.Update the components <br>
 7.Update the pipeline <br>
 8.Update the main.py <br>
 9.Update the dvc.yaml (dvc/data version control-  for pipeline tracking) <br>


## MLflow
- [Documentation](https://mlflow.org/docs/latest/index.html)


- MLflow learning

cmd

- mlflow ui

## dagshub

- [dagshub](https://dagshub.com/dashboard)

```cmd
MLFLOW_TRACKING_URI=https://dagshub.com/swaroopyadav/chest-Disease-Classification-MLflow-DVC.mlflow
MLFLOW_TRACKING_USERNAME=swaroopyadav
MLFLOW_TRACKING_PASSWORD=6824692c47a4545eac5b10041d5c8edbcef0
python script.py
```


# Add MLFlow credientials to your local_machine env variables: <br>

- Open env and add <br>

MLFLOW_TRACKING_URI=https://dagshub.com/swaroopyadav/chest-Disease-Classification-MLflow-DVC.mlflow

MLFLOW_TRACKING_USERNAME=swaroopyadav

MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9353c5b10041d5c8edbcef0


## DVC (data version control - Pipeline Tracking)
1) dvc init <br>
2) dvc repro <br>
3) dvc dag  <br>

