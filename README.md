# v-tag-editor

> Dead simple Vue.js tag editor component

## Demo

https://htmlpreview.github.io/?https://github.com/vuejs-tips/v-tag-editor/master/demo/index.html

## Usage

Just bind an array of tags using `v-model` directive or **value** property.

There's a separator property default to use *space*, but you can change it to *comma*.

```html
<template>
  <div>
    <v-tag-editor v-model="tags" theme="semantic-ui"></v-tag-list>
  </div>
</template>

<script>
import VTagEditor from 'v-tag-editor'

export default {
  components: {VTagEditor},
  data () {
    return {
      tags: ['php', 'ruby', 'javascript', 'python', 'java', 'c#', 'scala', 'closure']
    }
  }
}
</script>
```

## Installation

### Using yarn

`yarn add v-tag-editor`

### Using npm

`npm i --save v-tag-editor`

## License

This project is licensed under [MIT License](http://en.wikipedia.org/wiki/MIT_License)
