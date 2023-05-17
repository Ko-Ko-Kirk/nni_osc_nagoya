# This is a live demo code for OSC Nagoya 2023

## Modify and simplify from https://github.com/microsoft/nni/

## Install NNI
```
pip install --upgrade nni
```

## Run NNI
```
nnictl create --config config.yml --port 5566
```

## Check NNI
```
nnictl experiment list
```

## Check NNI WebUI
```
http://localhost:5566
```

## Stop NNI
```
nnictl stop
```

## Run on Azure Machine learning
1. Add your Azure Machine Learning workspace information in config.yml
```
training_service:
     platform: aml
     dockerImage: msranni/nni
     subscriptionId: your-subscription-id
     resourceGroup: your-resource-group
     workspaceName: your-workspace-name
     computeTarget: your-compute-target
```

2. Install Azure ML SDK
```
pip install azureml
pip install azureml-sdk
```

3. Login Azure ML
```
az login
```

4. Run NNI
```
nnictl create --config config.yml
```

5. Check NNI in Azure ML Studio

