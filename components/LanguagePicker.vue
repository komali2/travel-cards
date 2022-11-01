<script setup lang="ts">
import _ from 'lodash'

enum languages {
  'en_US'= 'English',
  'zh_TW' = 'Mandarin, Traditional',
}

const values = ref([])
const props = defineProps<{label: string, choices: keyof languages[]}>()

const mappedItems = _.map(_.pick(languages, props.choices), (val, key) => { return { title: val, value: key } })

</script>
<template>
  <div>
    <v-autocomplete
      v-model="values"
      :items="mappedItems"
      outlined
      dense
      chips
      small-chips
      :label="label"
      multiple
    />
  </div>
</template>
