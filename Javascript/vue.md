# Vue JS

### Refresh object properties as dictionary

Objects properties on Vue are not reactive. Whe you update an object property value, vue will not refresh all components/parts taht are using this object. The solution is use the Vue.set and/or Vue.delete.

```javascript

// To update
Vue.set(object, member, value);

// To delete
Vue.delete(object, member);
```
