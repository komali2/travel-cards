<script setup>
const allergies = ref([])

</script>
<template>
  <div>
    <input type="checkbox" id="hazelnut" value="hazelnut" v-model="allergies" />
    <label for="hazelnut">Hazelnut</label>
    <input type="checkbox" id="peanut" value="peanut" v-model="allergies" />
    <label for="peanut">peanut</label>
    <input type="checkbox" id="hotdog" value="hotdog" v-model="allergies" />
    <label for="hotdog">hotdog</label>
    <div>
      Allergies: {{allergies}}
    </div>
    <v-container>
      <v-row>
        <v-col cols="4">
          <LanguagePicker label="Choose your native language" />
        </v-col>
        <v-col cols="4">
          <LanguagePicker label="Choose the language to translate to" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
