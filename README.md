# gcp_weatherapp

## Steps to deploy the app on Google Cloud Platform

### Step 1: Generate libraries
```
pip install -t lib -r requirements.txt
```

### Step 2: Create project
```
Project ID: tokyoweather
```

### Step 3: Create file: *app.yaml*
```yaml
runtime: python37
```

### Step 5: Deploy
```shell
$ gcloud app deploy --project <Project_ID> -v 1
```
