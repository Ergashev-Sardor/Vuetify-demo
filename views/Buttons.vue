<template>
  <div>
    <!--
    Todo:
     1. Сверстать блок кнопок используя GRID блоки -
     2. Добавить разные вариации кнопок -
     3. Воспользваться имеющимися props-ами из библиотеки vuetify
     4. @click с разными действиями (например вызов alert, prompt, console.log, console.dir, console.error, console.warn, console.table, console.time)

    -->
    <div class="button-wrapper">
      <v-btn @click="callAlert('Hello world')">
        Button
      </v-btn>
      <v-btn variant="outlined" @click="console.log('Hello world My name is Sardor')">
        Button
      </v-btn>
      <v-btn height="80px" @click="console.error">
        Button
      </v-btn>
      <v-btn disabled="" @click="">
        Button
      </v-btn>
      <v-btn color="green" @click="console.time">
        Button
      </v-btn>
      <v-btn icon @click="console.table">
        <v-icon>mdi-vuetify</v-icon>
      </v-btn>
      <v-btn prepend-icon="mdi-vuetify" @click="console.dir('HELLO WORLD HAHAHAHAH')">
        Button
      </v-btn>
      <v-btn prepend-icon="mdi-vuetify" append-icon="mdi-vuetify" @click="">
        Button
      </v-btn>
      <v-btn stacked @click="callAlert('What is your name ???')">
        Button
      </v-btn>
      <v-btn height="72" min-width="164" @click="">
        With Ripple
      </v-btn>
      <v-btn :ripple="false" height="72" min-width="164" @click="">
        Without Ripple
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  methods:{
    callAlert(text) {
      alert(text)
    }
  }
}
</script>

<style>
.button-wrapper {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-column-gap: 45px;
  grid-row-gap: 20px;

}
</style>