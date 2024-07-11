# chicken_disease_classify

## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml


## Run from terminal:

docker build -t chickenapp01.azurecr.io/chicken:latest .

docker login chickenapp01.azurecr.io

docker push chickenapp01.azurecr.io/chicken:latest
