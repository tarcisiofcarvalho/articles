# IBM Forms


#### Get the data Line ID (Short ID)

```javascript
id = form.getServiceConfiguration("SC_ServiceConfig0").callService();
```
#### Get the stage buttons in the Form

```javascript
var actions = form.getStageActions();

for(var i=0; i<actions.length; i++){
   alert(get(actions,i).getId());
   if(get(actions,i).getId() === 'S_Submit'){
     get(actions,i).setVisible(false);
   }
}
```
