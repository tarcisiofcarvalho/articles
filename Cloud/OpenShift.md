# Open Shift


### Design - oc new-app

```sh
# From source code
oc new-app http://gitserver.example.com/mygitrepo

# Specify the image base
oc new-app -i php http://gitserver.example.com/mygitrepo
oc new-app php~http://gitserver.example.com/mygitrepo

# Specify the image and language runtime base
oc new-app -i php:7.0 http://gitserver.example.com/mygitrepo
oc new-app php:7.0~http://gitserver.example.com/mygitrepo

# Complete sample
oc new-app -i python:3.7 --strategy code --code http://gitserver.example.com/mygitrepo
```
