# DVC
The purpose of creating this repository is to gain the basic knowledge about the DVC.

### Pre-requisite libraries
`dvc == 2.0.5`

`matplotlib == 3.5.2`

`mlflow == 1.26.1`

`numpy == 1.22.1`

`pandas == 1.4.2`

`PyDrive2 == 1.10.1`

`scikit-learn == 1.1.1`

### Step to execute 
`dvc pull`

### Steps that I followed to push the data on cloud using DVC
* initialise the DVC `dvc init`
* Add the data in dvc `dvc add data/water_potability.csv`
* It will create the .dvc version of the data.
* After that, add the data on remote storage 
`dvc remote add --default myremote \
gdrive://0AIac4JZqHhKmUk9PDA/dvcstore`
* I have uploaded my dataset on google drive using above command.
* Perform operation that add the dvc storage on git as well using below command:
`git add .dvc/config`
* Next step is to store the data on dvc using `dvc push`
* Finally, Commit and push the changes on Git repository.
`git commit -m "Configure remote storage"`
`git push`

### Implementation
* This repository consists of the jupyter notebook that basically performs some ML operations.

### References
https://dvc.org/doc/api-reference

