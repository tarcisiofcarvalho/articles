# Python Build

### Procfile

This file should be stored at project root directory and have the command to start the python application when deployed on a cloud environment as IBM Cloud.

```sh
web: python app.py
```
Where **app.py** is the web app to be started


### Manifest

This file contains the environment setup details as variables to be used by the application.

```property
applications:
- path: .
  memory: 256M
  instances: 1
  domain: mydomain.com
  name: app name
  host: app host
  disk_quota: 2G
  buildpack: python_buildpack
  env:
   VAR1: value1
   VAR2: value2
````
