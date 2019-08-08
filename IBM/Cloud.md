#IBM Cloud


# Deploy an app

```sh
# Login in on IBM cloud
cf login -a <api.host.com> -s <space> -o <org> -u <user> -p <password>

# Push the app
cf push -f manifest.yml
```
