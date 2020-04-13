# Vue JS

vue reference:

```html
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

### Refresh object properties as dictionary

Objects properties on Vue are not reactive. Whe you update an object property value, vue will not refresh all components/parts taht are using this object. The solution is use the Vue.set and/or Vue.delete.

```javascript

// To update
Vue.set(object, member, value);

// To delete
Vue.delete(object, member);
```

### REST Request

Using axio library for api call.

first, set the reference:

```html
    <script src="https://cdn.jsdelivr.net/npm/axios@0.12.0/dist/axios.min.js"></script>
```

```javascript
axios.get(url).then(response => (x=response.data)
```

### REST Request with body data

```javascript
        var body = {
              'approver': approver
        };
        axios({
          method: 'post',
          url: '/your_url',
          data: body,
          headers: {'Content-Type': 'application/json'}
        }).then(response => (alert(response.status)));
```

### Vue component

```javascript
Vue.component('component-tag', {

    props: ['name'],
    template: `
               <tr>
                    <td>{{ name }}</td>
                    <td>
                        <button type="button" class="ds-icon-close" v-on:click="this.app.removeDistUser(name)"/>
                    </td>
               </tr>
               `,

})
```
