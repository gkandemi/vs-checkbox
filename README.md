# vs-checkbox

This is Checkbox Component created by VueJS

## Getting Started

These instructions will get you a copy of the component up and running on your local machine.

### Installing

You can install vs-checkbox component by npm

```
npm i vs-checkbox
```

After download, vs-checkbox will be ready to use in your VueJS Applications

### Usage

* Just import Components from node_modules folder in main.js

```
import Checkbox from "vs-checkbox"
```

* Register vs-checkbox component with any name you want

```
Vue.component("checkbox", Checkbox);
```

After this step, vs-checkbox can be used by all registered component in your project with checkbox tag name

* You can use with <checkbox></checkbox>

```
<checkbox></checkbox>
```

#### Styling

vs-checkbox has 6 color options

* primary
* secondary
* success
* danger
* info
* warning

To use these colors, just add 'color' attribute into checkbox component

```
<checkbox color="primary"></checkbox>
```

```
<checkbox color="secondary"></checkbox>
```

```
<checkbox color="success"></checkbox>
```

```
<checkbox color="danger"></checkbox>
```

```
<checkbox color="info"></checkbox>
```

```
<checkbox color="warning"></checkbox>
```

#### Data Binding

Also you can bind any data to vs-checkbox component by v-model VueJS directive

```
<script>
  export default {
    data(){
      return {
       status : true
      }
    }

  }
</script>
```

```
<checkbox v-model="status"></checkbox>
```

This data property will give us value as boolean (true or false)

#### Label Support (Optional)

As you wish, label can be used with vs-checkbox component.

```
<checkbox text="I read conditions and agreed"></checkbox>
```

If you add "text" attribute in checkbox tag, component will add a label with your text


## Versioning

We use [GitHub](https://github.com/gkandemi/vs-checkbox) for versioning. For the versions available, see the [tags on this repository](https://github.com/gkandemi/vs-checkbox/tags).

## Authors

* **Gökhan Kandemir** - [Gökhan Kandemir](https://github.com/gkandemi)

## License

This project is licensed under the MIT License

