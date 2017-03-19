<template lang="html">
<div class="v-tag-editor">
  <v-tag-input v-model="editableTags" :separator="separator"></v-tag-input>
  <v-tag-list v-model="editableTags" :theme="theme"></v-tag-list>
</div>
</template>

<script>
import VTagInput from 'v-tag-input'
import VTagList from 'v-tag-list'

export default {
  name: 'v-tag-editor',
  components: {VTagInput, VTagList},
  props: {
    value: {
      type: Array,
      default: () => [],
      required: true
    },
    theme: {
      type: [String, Object],
    },
    separator: {
      type: String,
      default: ' '
    }
  },

  computed: {
    editableTags: {
      get () {
        return this.value || []
      },

      set (newValue) {
        var clonedValue = newValue.slice()
        this.$emit('input', clonedValue)
      }
    }
  }
}
</script>
