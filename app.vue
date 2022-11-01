<script setup>
const allergies = ref([])

</script>
<template>
  <div>
    <input id="hazelnut" v-model="allergies" type="checkbox" value="hazelnut">
    <label for="hazelnut">Hazelnut</label>
    <input id="peanut" v-model="allergies" type="checkbox" value="peanut">
    <label for="peanut">peanut</label>
    <input id="hotdog" v-model="allergies" type="checkbox" value="hotdog">
    <label for="hotdog">hotdog</label>
    <div>
      Allergies: {{ allergies }}
    </div>
    <v-container>
      <v-row>
        <v-col cols="4">
          I speak...
          <LanguagePicker label="Choose your native language" :choices="['en_US']" />
        </v-col>
        <v-col cols="4">
          I'm traveling to a place that speaks...
          <LanguagePicker label="Choose the language to translate to" :choices="['en_US', 'zh_TW']" />
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          I need to communicate the following:
        </v-col>
        <v-col cols="12">
          <CheckboxList options="" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
