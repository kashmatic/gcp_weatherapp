# gcp_weatherapp

## Steps to deploy the app on Google Cloud Platform

### Step 1: Generate libraries
```
pip install -t lib -r requirements.txt
```

### Step 2: Create project
```
Project ID: weather-234603
```

### Step 3: Create file: *app.yaml*
```yaml
runtime: python37
api_version: 1
threadsafe: true

handlers:
- url: /static
  static_dir: static
- url: /.*
  script: main.app

libraries:
- name: ssl
  version: latest
```

### Step 4: Create app config file: *appengine_config.py*
```python
from google.appengine.ext import vendor

vendor.add('lib')
```

### Step 5: Deploy
```shell
$ gcloud config set project weatherapp-234600
Updated property [core/project].

$ gcloud init

$ gcloud app deploy app.yaml
```
