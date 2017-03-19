<template lang="html">
<div style="padding-top: 50px" class="container">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.3.2/css/bulma.min.css" rel="stylesheet">
  <h1 class="title">DEMO v-tag-editor Vue.js Component</h1>

  <p class="content">
    <v-tag-editor v-model="tags" theme="bulma"></v-tag-editor>
  </p>

  <p class="box">
    {{ tags }}
  </p>
</div>
</template>

<script>

import Component from '../src/Component.vue'

export default {
  components: {'v-tag-editor': Component},
  data () {
    return {
      tags: ['php', 'ruby', 'javascript', 'python', 'java', 'c#', 'scala', 'closure']
    }
  }
}
</script>

<style>
.v-tag-input {
  display: block;
  width: 100%;
  box-sizing: border-box;
  padding: 5px;
  margin-bottom: 5px;
  font-size: inherit;
  font-weight: bold;
  word-spacing: 5px;
}
.v-tag-input:focus {
  outline: 1px solid gray;
}
</style>
